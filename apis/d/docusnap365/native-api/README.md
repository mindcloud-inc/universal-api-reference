# Docusnap365: Native API Reference

A consolidated summary of Docusnap365's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api-doc.docusnap.com/reference/first-steps
- **API base URL:** `https://api.docusnap365.com`

## Authentication

### API Key

Authenticate Docusnap365 requests with an API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api-doc.docusnap.com/reference/sites)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Data Details](actions/get-data-details.md) | `GET /api/v2/segment/data/:id/detailed` | [docs](https://api-doc.docusnap.com/reference/datadetailsexample) |
| [Get Network Details](actions/get-network-details.md) | `GET /api/v2/segment/networks/:id/detailed` | [docs](https://api-doc.docusnap.com/reference/networkdetailsexample) |
| [Get Service Details](actions/get-service-details.md) | `GET /api/v2/segment/services/:id/detailed` | [docs](https://api-doc.docusnap.com/reference/servicedetailsexample) |
| [Get System Details](actions/get-system-details.md) | `GET /api/v2/segment/systems/:id/detailed` | [docs](https://api-doc.docusnap.com/reference/systemdetailsexample) |
| [List Data](actions/list-data.md) | `GET /api/v2/segment/data` | [docs](https://api-doc.docusnap.com/reference/datalist) |
| [List Data By Type](actions/list-data-by-type.md) | `GET /api/v2/segment/data/type/:typeId` | [docs](https://api-doc.docusnap.com/reference/getdatabytype) |
| [List Data Types](actions/list-data-types.md) | `GET /api/v2/segment/data/types` | [docs](https://api-doc.docusnap.com/reference/datatypes) |
| [List Domains](actions/list-domains.md) | `GET /api/v2/domains` | [docs](https://api-doc.docusnap.com/reference/domains) |
| [List Network Types](actions/list-network-types.md) | `GET /api/v2/segment/networks/types` | [docs](https://api-doc.docusnap.com/reference/networktypes) |
| [List Networks](actions/list-networks.md) | `GET /api/v2/segment/networks` | [docs](https://api-doc.docusnap.com/reference/networklist) |
| [List Networks By Type](actions/list-networks-by-type.md) | `GET /api/v2/segment/networks/type/:typeId` | [docs](https://api-doc.docusnap.com/reference/getnetworksbytype) |
| [List Organizations](actions/list-organizations.md) | `GET /api/v2/organizations` | [docs](https://api-doc.docusnap.com/reference/organizations) |
| [List Platforms](actions/list-platforms.md) | `GET /api/v2/platforms` | [docs](https://api-doc.docusnap.com/reference/platforms) |
| [List Service Types](actions/list-service-types.md) | `GET /api/v2/segment/services/types` | [docs](https://api-doc.docusnap.com/reference/servicetypes) |
| [List Services](actions/list-services.md) | `GET /api/v2/segment/services` | [docs](https://api-doc.docusnap.com/reference/serviceslist) |
| [List Services By Type](actions/list-services-by-type.md) | `GET /api/v2/segment/services/type/:typeId` | [docs](https://api-doc.docusnap.com/reference/getservicebytype) |
| [List Sites](actions/list-sites.md) | `GET /api/v2/sites` | [docs](https://api-doc.docusnap.com/reference/sites) |
| [List System Types](actions/list-system-types.md) | `GET /api/v2/segment/systems/types` | [docs](https://api-doc.docusnap.com/reference/systemtypes) |
| [List Systems](actions/list-systems.md) | `GET /api/v2/segment/systems` | [docs](https://api-doc.docusnap.com/reference/systemslist) |
| [List Systems By Type](actions/list-systems-by-type.md) | `GET /api/v2/segment/systems/type/:typeId` | [docs](https://api-doc.docusnap.com/reference/getsystemsbytype) |
