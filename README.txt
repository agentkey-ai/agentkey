AGENTKEY WEBSITE PACKAGE

Files:
- index.html: responsive AgentKey landing page with dark navy, silver/blue and gold styling.
- favicon.ico: browser tab icon.
- favicon.png: high-resolution icon.
- favicon-32.png: 32x32 browser icon.
- apple-touch-icon.png: mobile home-screen icon.
- robots.txt: allows search engine crawling and points to the sitemap.
- sitemap.xml: homepage sitemap for agentkey.xyz.

Deployment:
1. Upload the files to the root of the GitHub repository, next to index.html.
2. Commit the changes.
3. Cloudflare Pages will redeploy automatically when Git integration is enabled.

Important:
The landing page is configured to read totalMinted(), freeMintsRemaining(), currentMintPrice(1), MINT_START_TIME(), and MAX_SUPPLY() from the supplied AgentKey contract on BNB Smart Chain Mainnet. It prepares an AI-agent prompt for the mint(uint256) function; it does not directly submit wallet transactions. The website cannot independently certify the deployed contract as safe. Verify the contract and exact payment in the wallet before approving any transaction. Marketplace transactions and on-chain staking UI remain unconnected.
