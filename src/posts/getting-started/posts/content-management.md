---
title: "Implementation"
summary: "Today more people and experts write about accessibility. For the better progression it is a good idea to read them."
eleventyNavigation:
  key: Implementation
  parent: Getting Started
  order: 5
---

- We have started with a standard Hardhat project and added essential methods to the StealthAddress contract. To enhance credibility, we intentionally avoided making the contract upgradeable, as there's no on-chain governance currently. If an upgrade is needed, we'll deploy a new version and provide client-side support.

- Next, we developed the UI/UX using React and TypeScript, focusing on a simple yet elegant design for both power and non-power users. The UI colors and feel are built with the XRP EVM compatible chain in mind.

- We used the Wagmi library for blockchain interactions which streamlined the process.

- The elliptic library handled the complex math involved with elliptic curves, and both libraries featured TypeScript typings, making them a joy to work with.

- We used Streamr Client to store all user transactions in a Data Pool on Streamr Hub

- Tools Used: Solidity, Hardhat, XRP EVM compatible chain, React, Typescript, Wagmi, and Metamask.