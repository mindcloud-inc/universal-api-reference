# Interzoid: Native API Reference

A consolidated summary of Interzoid's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.interzoid.com/
- **API base URL:** `https://api.interzoid.com`

## Authentication

### API Key

Authenticate Interzoid with an API license key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.interzoid.com/cloud-api-directory)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compare Full Names](actions/compare-full-names.md) | `GET /getfullnamematchscore` | [docs](https://www.interzoid.com/apis/individual-match-score) |
| [Compare Organization Names](actions/compare-organization-names.md) | `GET /getorgmatchscore` | [docs](https://www.interzoid.com/apis/organization-match-score) |
| [Get Business Info](actions/get-business-info.md) | `GET /getbusinessinfo` | [docs](https://www.interzoid.com/apis/get-business-info) |
| [Get Company And Address Match Similarity Key](actions/get-company-and-address-match-similarity-key.md) | `GET /getcompanyandaddressmatch` | [docs](https://www.interzoid.com/apis/company-and-address-matching) |
| [Get Company And Full Name Match Similarity Key](actions/get-company-and-full-name-match-similarity-key.md) | `GET /getcompanyandfullnamematch` | [docs](https://www.interzoid.com/apis/company-and-fullname-matching) |
| [Get Company Match Similarity Key](actions/get-company-match-similarity-key.md) | `GET /getcompanymatchadvanced` | [docs](https://www.interzoid.com/apis/company-name-matching) |
| [Get Full Name And Address Match Similarity Key](actions/get-full-name-and-address-match-similarity-key.md) | `GET /getaddressandfullnamematch` | [docs](https://www.interzoid.com/apis/address-and-fullname-matching) |
| [Get Full Name Match Similarity Key](actions/get-full-name-match-similarity-key.md) | `GET /getfullnamematch` | [docs](https://www.interzoid.com/apis/individual-name-matching) |
| [Get Global Address Match Similarity Key](actions/get-global-address-match-similarity-key.md) | `GET /getglobaladdressmatch` | [docs](https://www.interzoid.com/apis/global-address-matching) |
| [Get Remaining Credits](actions/get-remaining-credits.md) | `GET /getremainingcredits` | [docs](https://www.interzoid.com/apis/remaining-api-credits) |
| [Get Street Address Match Similarity Key](actions/get-street-address-match-similarity-key.md) | `GET /getaddressmatchadvanced` | [docs](https://www.interzoid.com/apis/street-address-matching) |
