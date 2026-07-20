# Pinata: Native API Reference

A consolidated summary of Pinata's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.pinata.cloud/api-reference/introduction
- **API base URL:** `https://api.pinata.cloud`

## Authentication

### JWT Bearer Token

Use a Pinata JWT generated from the API Keys page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pinata.cloud/account-management/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `pageToken` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File To Group](actions/add-file-to-group.md) | `PUT /v3/groups/:network/:id/ids/:fileId` | [docs](https://docs.pinata.cloud/api-reference/endpoint/add-file-to-group) |
| [Add Signature to CID](actions/add-signature-to-cid.md) | `POST /v3/files/:network/signature/:cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/add-signature-to-cid) |
| [Add Swap](actions/add-swap.md) | `PUT /v3/files/:network/swap/:cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/add-swap) |
| [Cancel Pin Request](actions/cancel-pin-request.md) | `DELETE /v3/files/public/pin_by_cid/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/cancel-pin-by-cid) |
| [Create Gateway](actions/create-gateway.md) | `POST /v3/gateways` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/create-gateway) |
| [Create Group](actions/create-group.md) | `POST /v3/groups/:network` | [docs](https://docs.pinata.cloud/api-reference/endpoint/create-group) |
| [Delete File by ID](actions/delete-file-by-id.md) | `DELETE /v3/files/:network/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/delete-file-by-id) |
| [Delete Gateway](actions/delete-gateway.md) | `DELETE /v3/gateways/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/delete-gateway) |
| [Delete Group](actions/delete-group.md) | `DELETE /v3/groups/:network/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/delete-group) |
| [Get Data Usage](actions/get-data-usage.md) | `GET /data/userPinnedDataTotal` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/data-usage) |
| [Get File by ID](actions/get-file-by-id.md) | `GET /v3/files/:network/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/get-file-by-id) |
| [Get Gateway Details](actions/get-gateway-details.md) | `GET /v3/gateways/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/gateway-details) |
| [Get Gateway Domain Availability](actions/get-gateway-domain-availability.md) | `GET /v3/gateways/exists/:domain` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/gateway-domain-available) |
| [Get Group](actions/get-group.md) | `GET /v3/groups/:network/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/get-group) |
| [Get Signature for a CID](actions/get-signature-for-a-cid.md) | `GET /v3/files/:network/signature/:cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/get-signature-for-a-cid) |
| [Get Swap History](actions/get-swap-history.md) | `GET /v3/files/:network/swap/:cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/get-swap-history) |
| [Get Time Interval Gateway Analytics](actions/get-time-interval-gateway-analytics.md) | `GET /v3/analytics/gateways/time_series` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/time-interval-gateway-analytics) |
| [Get Top Gateway Analytics](actions/get-top-gateway-analytics.md) | `GET /v3/analytics/gateways/top` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/top-gateway-analytics) |
| [List Files](actions/list-files.md) | `GET /v3/files/:network` | [docs](https://docs.pinata.cloud/api-reference/endpoint/list-files) |
| [List Gateways](actions/list-gateways.md) | `GET /v3/gateways` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/list-gateways) |
| [List Groups](actions/list-groups.md) | `GET /v3/groups/:network` | [docs](https://docs.pinata.cloud/api-reference/endpoint/list-groups) |
| [Pin by CID](actions/pin-by-cid.md) | `POST /v3/files/public/pin_by_cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/pin-by-cid) |
| [Pin JSON](actions/pin-json.md) | `POST /pinning/pinJSONToIPFS` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/pin-json-to-ipfs) |
| [Remove File From Group](actions/remove-file-from-group.md) | `DELETE /v3/groups/:network/:id/ids/:fileId` | [docs](https://docs.pinata.cloud/api-reference/endpoint/remove-file-from-group) |
| [Remove Signature from CID](actions/remove-signature-from-cid.md) | `DELETE /v3/files/:network/signature/:cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/remove-signature-from-cid) |
| [Remove Swap](actions/remove-swap.md) | `DELETE /v3/files/:network/swap/:cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/remove-swap) |
| [Search Pin Requests](actions/search-pin-requests.md) | `GET /v3/files/public/pin_by_cid` | [docs](https://docs.pinata.cloud/api-reference/endpoint/query-pin-requests) |
| [Test Authentication](actions/test-authentication.md) | `GET /data/testAuthentication` | [docs](https://docs.pinata.cloud/api-reference/endpoint/ipfs/test-authentication) |
| [Update File](actions/update-file.md) | `PUT /v3/files/:network/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/update-file) |
| [Update Group](actions/update-group.md) | `PUT /v3/groups/:network/:id` | [docs](https://docs.pinata.cloud/api-reference/endpoint/update-group) |
