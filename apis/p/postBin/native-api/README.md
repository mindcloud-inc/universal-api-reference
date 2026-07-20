# PostBin: Native API Reference

A consolidated summary of PostBin's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.postb.in/api
- **API base URL:** `https://www.postb.in/api/`

## Authentication

### No Authentication

Public PostBin API access does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.postb.in/api)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bin](actions/create-bin.md) | `POST /bin` | [docs](https://www.postb.in/api) |
| [Delete Bin](actions/delete-bin.md) | `DELETE /bin/:binId` | [docs](https://www.postb.in/api) |
| [Get Bin](actions/get-bin.md) | `GET /bin/:binId` | [docs](https://www.postb.in/api) |
| [Get Request](actions/get-request.md) | `GET /bin/:binId/req/:reqId` | [docs](https://www.postb.in/api) |
| [Shift Request](actions/shift-request.md) | `GET /bin/:binId/req/shift` | [docs](https://www.postb.in/api) |
