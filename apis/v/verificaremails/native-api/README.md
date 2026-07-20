# Verificaremails: Native API Reference

A consolidated summary of Verificaremails's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://dashboard.verificaremails.com/documentation/index.html
- **OpenAPI specification:** https://dashboard.verificaremails.com/documentation/openai.json
- **API base URL:** `https://dashboard.verificaremails.com/myapi`

## Authentication

### API Key

Authenticate Verificaremails requests with your API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dashboard.verificaremails.com/documentation/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Address Batch Validation](actions/create-address-batch-validation.md) | `POST /address/validate/multiple` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Create Email Batch Validation](actions/create-email-batch-validation.md) | `POST /email/validate/multiple` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Create Name Batch Validation](actions/create-name-batch-validation.md) | `POST /name/validate/multiple` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Create Phone Batch Validation](actions/create-phone-batch-validation.md) | `POST /phone/validate/multiple` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Create Phone MNP Batch Validation](actions/create-phone-mnp-batch-validation.md) | `POST /phonemnp/validate/multiple` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Create Phone Syntactic Batch Validation](actions/create-phone-syntactic-batch-validation.md) | `POST /phonesyntactic/validate/multiple` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Address Batch Status](actions/get-address-batch-status.md) | `GET /address/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Address Credits](actions/get-address-credits.md) | `GET /address/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get All Credits](actions/get-all-credits.md) | `GET /all/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html) |
| [Get Complete Name Batch Status](actions/get-complete-name-batch-status.md) | `GET /namecomplete/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Complete Name Credits](actions/get-complete-name-credits.md) | `GET /namecomplete/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Email Batch Status](actions/get-email-batch-status.md) | `GET /email/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Email Credits](actions/get-email-credits.md) | `GET /email/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Fuzzy Search Name Batch Status](actions/get-fuzzy-search-name-batch-status.md) | `GET /fuzzysearch/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Fuzzy Search Name Credits](actions/get-fuzzy-search-name-credits.md) | `GET /fuzzysearch/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Name Batch Status](actions/get-name-batch-status.md) | `GET /name/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Name Credits](actions/get-name-credits.md) | `GET /name/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Phone Batch Status](actions/get-phone-batch-status.md) | `GET /phone/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Phone Credits](actions/get-phone-credits.md) | `GET /phone/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Phone MNP Batch Status](actions/get-phone-mnp-batch-status.md) | `GET /phonemnp/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Phone MNP Credits](actions/get-phone-mnp-credits.md) | `GET /phonemnp/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Phone Syntactic Batch Status](actions/get-phone-syntactic-batch-status.md) | `GET /phonesyntactic/status/{{requestId}}` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Get Phone Syntactic Credits](actions/get-phone-syntactic-credits.md) | `GET /phonesyntactic/credits` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Address Input](actions/validate-single-address-input.md) | `GET /address/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Complete Name Input](actions/validate-single-complete-name-input.md) | `GET /namecomplete/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Email Input](actions/validate-single-email-input.md) | `GET /email/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Fuzzy Search Name Input](actions/validate-single-fuzzy-search-name-input.md) | `GET /fuzzysearch/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Name Input](actions/validate-single-name-input.md) | `GET /name/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Phone Input](actions/validate-single-phone-input.md) | `GET /phone/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Phone MNP Input](actions/validate-single-phone-mnp-input.md) | `GET /phonemnp/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
| [Validate Single Phone Syntactic Input](actions/validate-single-phone-syntactic-input.md) | `GET /phonesyntactic/validate/single` | [docs](https://dashboard.verificaremails.com/documentation/index.html?v=6) |
