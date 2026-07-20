# Qive: Native API Reference

A consolidated summary of Qive's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.qive.com.br/docs/get/v1/nfe/received
- **API base URL:** `https://sandbox-api.arquivei.com.br`

## Authentication

### API Key Pair

Authenticate Qive REST API requests with the x-api-id and x-api-key headers.

### Credentials

- **API Key:** `apiKey` · required
- **API ID:** `apiId` · required · Qive API ID used in the x-api-id request header.

Send these headers with each API request:

```http
x-api-id: <apiId>
x-api-key: <apiKey>
```

[Official authentication documentation](https://developers.qive.com.br/help)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `page.next`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–50). Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Companies](actions/get-companies.md) | `GET /v1/company` | [docs](https://developers.qive.com.br/docs/get/v1/company) |
| [Get CTe Upload Status](actions/get-cte-upload-status.md) | `GET /v1/cte/upload/status` | [docs](https://developers.qive.com.br/docs/get/v1/cte/upload/status) |
| [Get DACTe](actions/get-dacte.md) | `GET /v1/cte/dacte` | [docs](https://developers.qive.com.br/docs/get/v1/cte/dacte) |
| [Get DACTe-OS](actions/get-dacte-os.md) | `GET /v1/cte-os/dacteos` | [docs](https://developers.qive.com.br/docs/get/v1/cte-os/dacteos) |
| [Get DANFe](actions/get-danfe.md) | `GET /v1/nfe/danfe` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/danfe) |
| [Get DANFSe](actions/get-danfse.md) | `GET /v1/nfse/danfse` | [docs](https://developers.qive.com.br/docs/get/v1/nfse/danfse) |
| [Get Emitted NFSe Manual PDF](actions/get-emitted-nfse-manual-pdf.md) | `GET /v1/nfse/emitted/manual/pdf` | [docs](https://developers.qive.com.br/docs/get/v1/nfse/emitted/manual/pdf) |
| [Get NFe Manifest Status](actions/get-nfe-manifest-status.md) | `GET /v1/nfe/manifest/status` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/manifest/status) |
| [Get NFe Upload Status](actions/get-nfe-upload-status.md) | `GET /v1/nfe/upload/status` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/upload/status) |
| [Get Received NFSe Manual PDF](actions/get-received-nfse-manual-pdf.md) | `GET /v1/nfse/received/manual/pdf` | [docs](https://developers.qive.com.br/docs/get/v1/nfse/received/manual/pdf) |
| [List Authorized CTes](actions/list-authorized-ctes.md) | `GET /v1/cte/authorized` | [docs](https://developers.qive.com.br/docs/get/v1/cte/authorized) |
| [List Authorized NFes](actions/list-authorized-nfes.md) | `GET /v1/nfe/authorized` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/authorized) |
| [List CTe Events](actions/list-cte-events.md) | `GET /v1/cte/events` | [docs](https://developers.qive.com.br/docs/get/v1/cte/events) |
| [List CTe Events V2](actions/list-cte-events-v2.md) | `GET /v2/cte/events` | [docs](https://developers.qive.com.br/docs/get/v2/cte/events) |
| [List CTe-OS Events](actions/list-cte-os-events.md) | `GET /v1/cte-os/events` | [docs](https://developers.qive.com.br/docs/get/v1/cte-os/events) |
| [List Emitted NFes](actions/list-emitted-nfes.md) | `GET /v1/nfe/emitted` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/emitted) |
| [List Emitted NFSes](actions/list-emitted-nfses.md) | `GET /v1/nfse/emitted` | [docs](https://developers.qive.com.br/docs/get/v1/nfse/emitted) |
| [List NFe Events V2](actions/list-nfe-events-v2.md) | `GET /v2/nfe/events` | [docs](https://developers.qive.com.br/docs/get/v2/nfe/events) |
| [List NFe Manifests](actions/list-nfe-manifests.md) | `GET /v1/nfe/manifest` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/manifest) |
| [List NFe Manifests V2](actions/list-nfe-manifests-v2.md) | `GET /v2/nfe/manifest` | [docs](https://developers.qive.com.br/docs/get/v2/nfe/manifest) |
| [List NFSe Events](actions/list-nfse-events.md) | `GET /v1/nfse/events` | [docs](https://developers.qive.com.br/docs/get/v1/nfse/events) |
| [List Not-Taker CTe-OS](actions/list-not-taker-cte-os.md) | `GET /v1/cte-os/not-taker` | [docs](https://developers.qive.com.br/docs/get/v1/cte-os/not-taker) |
| [List Not-Taker CTes](actions/list-not-taker-ctes.md) | `GET /v1/cte/not-taker` | [docs](https://developers.qive.com.br/docs/get/v1/cte/not-taker) |
| [List Properties](actions/list-properties.md) | `GET /v1/property` | [docs](https://developers.qive.com.br/docs/get/v1/property) |
| [List Received NFes](actions/list-received-nfes.md) | `GET /v1/nfe/received` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/received) |
| [List Received NFSes](actions/list-received-nfses.md) | `GET /v1/nfse/received` | [docs](https://developers.qive.com.br/docs/get/v1/nfse/received) |
| [List Received NFSes V2](actions/list-received-nfses-v2.md) | `GET /v2/nfse/received` | [docs](https://developers.qive.com.br/docs/get/v2/nfse/received) |
| [List Taker CTe-OS](actions/list-taker-cte-os.md) | `GET /v1/cte-os/taker` | [docs](https://developers.qive.com.br/docs/get/v1/cte-os/taker) |
| [List Taker CTes](actions/list-taker-ctes.md) | `GET /v1/cte/taker` | [docs](https://developers.qive.com.br/docs/get/v1/cte/taker) |
| [List Transporter NFes](actions/list-transporter-nfes.md) | `GET /v1/nfe/transporter` | [docs](https://developers.qive.com.br/docs/get/v1/nfe/transporter) |
