# KIS: Native API Reference

A consolidated summary of KIS's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://doc.getkis.io/documentation/documentation-api
- **API base URL:** `https://api.getkis.io/api/v1`

## Authentication

### App Token + Secret

Authenticate KIS requests by exchanging an app token and secret for a reusable authorization header.

### Credentials

- **App Token:** `appToken` · required · KIS app token from Settings -> API Keys.

Send these headers with each API request:

```http
Authorization: <custom.authorization>
```

[Official authentication documentation](https://doc.getkis.io/documentation/documentation-api/authentification/sauthentifier-a-lapi)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `text/plain` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Records](actions/create-records.md) | `POST /api_token_access/data_handlers` | [docs](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/creer-de-la-donnee) |
| [Delete Record](actions/delete-record.md) | `DELETE /api_token_access/data_handlers/{recordId}` | [docs](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/supprimer-une-donnee) |
| [List Records](actions/list-records.md) | `POST /api_token_access/data_handlers` | [docs](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/recuperer-les-donnees) |
| [List Tables](actions/list-tables.md) | `GET /api_token_access/collections` | [docs](https://doc.getkis.io/documentation/documentation-api/tables-de-donnees/lister-les-tables-de-donnees) |
| [Sign In](actions/sign-in.md) | `POST /api_access_auth/sign_in` | [docs](https://doc.getkis.io/documentation/documentation-api/authentification/sauthentifier-a-lapi) |
| [Update Record](actions/update-record.md) | `PUT /api_token_access/data_handlers/{recordId}` | [docs](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/mettre-a-jour-une-donnee) |
| [Wipe Table](actions/wipe-table.md) | `POST /api_token_access/collections/wipe/{tableId}` | [docs](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/supprimer-la-totalite-des-donnees-dune-table-de-donnees) |
