# Dropcontact: Native API Reference

A consolidated summary of Dropcontact's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://developer.dropcontact.com/
- **API base URL:** `https://api.dropcontact.com`

## Authentication

### API Key (Header Only)

Connect Dropcontact using your API key sent only in the X-Access-Token header.

### Credentials

- **API Key:** `apiKey` · optional · Dropcontact API key used for the X-Access-Token request header.

[Official authentication documentation](https://developer.dropcontact.com/)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enrich Contacts](actions/enrich-contacts.md) | `POST /v1/enrich/all` | [docs](https://developer.dropcontact.com/#post-request) |
| [Get Credits Left](actions/get-credits-left.md) | `POST /v1/enrich/all` | [docs](https://developer.dropcontact.com/#credits-left) |
| [Get Enrichment Request](actions/get-enrichment-request.md) | `GET /v1/enrich/all/{{requestId}}` | [docs](https://developer.dropcontact.com/#get-request) |
