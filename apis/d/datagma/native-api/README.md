# Datagma: Native API Reference

A consolidated summary of Datagma's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://datagmaapi.readme.io/reference/getting-started-with-your-api
- **API base URL:** `https://gateway.datagma.net/api/ingress`

## Authentication

### API Key

Use a Datagma API key from the Datagma dashboard to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://datagmaapi.readme.io/reference/getting-started-with-your-api)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enrich a person or a company](actions/enrich-a-person-or-a-company.md) | `GET /v2/full` | [docs](https://datagmaapi.readme.io/reference/ingressservice_fullapiv2) |
| [Find People](actions/find-people.md) | `GET /v1/find_people` | [docs](https://datagmaapi.readme.io/reference/ingressservice_findpeople) |
| [Find Work Verified Email](actions/find-work-verified-email.md) | `GET /v8/findEmail` | [docs](https://datagmaapi.readme.io/reference/ingressservice_findemailv8) |
| [Get Credit](actions/get-credit.md) | `GET /v1/mine` | [docs](https://datagmaapi.readme.io/reference/ingressservice_getcredit) |
| [Get Twitter By Email](actions/get-twitter-by-email.md) | `GET /v1/twitter/by_email` | [docs](https://datagmaapi.readme.io/reference/ingressservice_gettwitterbyemail) |
| [Get Twitter By Username](actions/get-twitter-by-username.md) | `GET /v1/twitter/by_username` | [docs](https://datagmaapi.readme.io/reference/ingressservice_gettwitterbyusername) |
| [Job Change Detection](actions/job-change-detection.md) | `GET /v4/update` | [docs](https://datagmaapi.readme.io/reference/ingressservice_stellaupdatev2) |
| [Search By Email (outside EU)](actions/search-by-email-outside-eu.md) | `GET /v1/reverse_email` | [docs](https://datagmaapi.readme.io/reference/ingressservice_searchbyemail) |
| [Search By Phone Numbers](actions/search-by-phone-numbers.md) | `GET /v1/reverse_phone_lookup` | [docs](https://datagmaapi.readme.io/reference/ingressservice_searchbyphone) |
| [Search Phone Numbers](actions/search-phone-numbers.md) | `GET /v1/search` | [docs](https://datagmaapi.readme.io/reference/ingressservice_search) |
