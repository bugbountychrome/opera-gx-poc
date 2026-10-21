# Opera GX Mobile - Address Bar Spoofing PoC

This repository contains the Proof of Concept (PoC) for the Address Bar Spoofing vulnerability via the `userinfo` (`@`) component reported to Opera Bug Bounty.

## Vulnerability Summary
Opera GX for Android fails to sanitize the `userinfo` component in the address bar. An attacker can craft a URL like:
`https://opera.com@attacker.com`

While the browser loads the content from `attacker.com`, the address bar visually displays `opera.com@attacker.com`, deceiving the user into believing they are on a legitimate Opera domain.

## Live Demonstration
You can test the live PoC directly in Opera GX Mobile:
[**Click here to open the Fake Login Page**](https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPO_NAME/)

*(Note: Replace `YOUR_GITHUB_USERNAME` and `YOUR_REPO_NAME` above with your actual GitHub Pages URL).*

When you visit this link via the vulnerable URL format, the page will render a fake Opera GX login screen and display an alert proving that the actual host is the GitHub Pages domain, not Opera.

## Evidence
See the attached screenshots in the Bugcrowd report for comparison between Opera GX (vulnerable) and Chrome (sanitized).
