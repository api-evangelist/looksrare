# LooksRare

LooksRare is a community-first NFT marketplace built on Ethereum that rewards traders, collectors, and creators. The platform operates an off-chain order book with on-chain settlement via the LooksRare V2 protocol and Seaport integration, supporting ERC-721 and ERC-1155 tokens.

## Public REST API

Base URL (Mainnet): `https://api.looksrare.org/api`
Base URL (Sepolia testnet): `https://api-sepolia.looksrare.org/api`

### Key Endpoints

| Version | Method | Path | Description |
|---------|--------|------|-------------|
| v2 | GET | /v2/orders | Retrieve asks and bids with filtering by collection, token, signer, and status |
| v2 | POST | /v2/orders | Submit a signed maker order (ask or bid) |
| v2 | GET | /v2/events | Retrieve LIST, SALE, OFFER, CANCEL_LIST, CANCEL_OFFER events |
| v2 | GET | /v2/orders/seaport | Retrieve Seaport-compatible orders |
| v2 | POST | /v2/orders/seaport | Create Seaport-compatible orders |
| v2 | GET | /v2/events/seaport | Retrieve Seaport events |
| v2 | GET | /v2/collections/seaport | Check if a collection supports Seaport trading |
| v1 | GET | /v1/tokens | Retrieve token metadata and attributes |
| v1 | GET | /v1/events | Legacy V1 protocol events, mints, and transfers |

### Authentication

- **Sepolia testnet**: No API key required
- **Mainnet read endpoints**: No API key required
- **Mainnet write endpoints** (POST /v2/orders): API key required — request via [developer Discord](https://discord.gg/LooksRareDevelopers)

### Rate Limits

A 10-second response cache is applied to all endpoints. HTTP 429 responses include a `Retry-After` header. Higher rate limits are available by request for production applications.

### Attribution

The API is free to use. In exchange, integrators must display a visible link to [looksrare.org](https://looksrare.org) alongside any NFT data shown on their platform.

## Resources

- [Marketplace](https://looksrare.org)
- [Developer Documentation](https://docs.looksrare.org/developers/welcome)
- [API Reference](https://looksrare.dev)
- [Changelog](https://looksrare.dev/changelog)
- [SDK v2 (GitHub)](https://github.com/LooksRare/sdk-v2)
- [SDK v2 (npm)](https://www.npmjs.com/package/@looksrare/sdk-v2)
- [Developer Discord](https://discord.gg/LooksRareDevelopers)
- [GitHub Organization](https://github.com/LooksRare)
