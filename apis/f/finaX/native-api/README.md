# finaX: Native API Reference

A consolidated summary of finaX's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.finax.dev/reference
- **OpenAPI specification:** https://docs.finax.dev/openapi.json
- **API base URL:** `https://api.finax.dev`

## Authentication

### API Key

Authenticate requests with a Finax API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.finax.dev/reference)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [CII Invoice Xml](actions/cii-invoice-xml.md) | `POST /v1/xml/cii/` | [docs](https://docs.finax.dev/reference) |
| [CII Or UBL To JSON](actions/cii-or-ubl-to-json.md) | `POST /v1/json/xml/` | [docs](https://docs.finax.dev/reference) |
| [CII To JSON](actions/cii-to-json.md) | `POST /v1/json/cii/` | [docs](https://docs.finax.dev/reference) |
| [Invoice XML From ZUGFeRD](actions/invoice-xml-from-zugferd.md) | `POST /v1/pdf/xml/` | [docs](https://docs.finax.dev/reference) |
| [Merge PDF And XML](actions/merge-pdf-and-xml.md) | `POST /v1/pdf/merge/` | [docs](https://docs.finax.dev/reference) |
| [PDF From CII](actions/pdf-from-cii.md) | `POST /v1/pdf/cii/` | [docs](https://docs.finax.dev/reference) |
| [PDF From JSON](actions/pdf-from-json.md) | `POST /v1/pdf/json/` | [docs](https://docs.finax.dev/reference) |
| [PDF From UBL](actions/pdf-from-ubl.md) | `POST /v1/pdf/ubl/` | [docs](https://docs.finax.dev/reference) |
| [UBL Invoice Xml](actions/ubl-invoice-xml.md) | `POST /v1/xml/ubl/` | [docs](https://docs.finax.dev/reference) |
| [UBL To JSON](actions/ubl-to-json.md) | `POST /v1/json/ubl/` | [docs](https://docs.finax.dev/reference) |
| [XML Metadata From ZUGFeRD](actions/xml-metadata-from-zugferd.md) | `POST /v1/pdf/metadata/` | [docs](https://docs.finax.dev/reference) |
| [ZUGFeRD To JSON](actions/zugferd-to-json.md) | `POST /v1/json/zugferd/` | [docs](https://docs.finax.dev/reference) |
