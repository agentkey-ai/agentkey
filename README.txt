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


MARKET DASHBOARD UPDATE (29 October 2026)
- The Market section now uses a responsive black-and-gold dashboard inspired by the supplied reference image.
- Marketplace metrics and sale rows intentionally show unavailable placeholders until a real Element API integration is configured. No fake sales, prices, buyers, or listing counts are displayed.
- Element's API requires an API key. Keep it in a server-side secret (such as a Cloudflare Worker secret) and proxy requests through a server-side endpoint. Do not place the API key in index.html or public JavaScript.
- Staking section has been left unchanged as requested.
- This update changes the Market presentation only; it does not implement marketplace order execution or verify the smart contract.


Latest update: Market is now a simple AI-agent selling-prompt page. Internal navigation uses clean paths (/home, /mint, /market, /staking, /collection, /about) instead of hash URLs. Cloudflare Pages should serve index.html as the SPA fallback for these paths; test direct URL refresh after deployment.
