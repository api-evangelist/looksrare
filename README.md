# LooksRare

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
