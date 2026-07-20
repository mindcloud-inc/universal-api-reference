# CommercioNetwork: Native API Reference

A consolidated summary of CommercioNetwork's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.commercio.network/app_developers/commercioapi-introduction.html
- **OpenAPI specification:** https://dev-api.commercio.app/v1/swagger/openapi.yaml
- **API base URL:** `https://dev-api.commercio.app/v1`

## Authentication

### Username & Password (JWT)

Use a Commercio dev-testnet account username and password to exchange for an OpenID id_token.

### Credentials

- **Username:** `username` · required · Commercio account email or username used to sign in to the dev web app.

Send these headers with each API request:

```http
Authorization: Bearer <custom.id_token>
```

[Official authentication documentation](https://docs.commercio.network/app_developers/commercioapi-authentication.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Receipt](actions/create-receipt.md) | `POST /receipts` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#send-a-receipt-message-process) |
| [Create Shared Document Process](actions/create-shared-document-process.md) | `POST /sharedoc/process` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#send-a-sharedoc-message) |
| [Get Receipt Process](actions/get-receipt-process.md) | `GET /receipts/process/:process_id` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#sent-receipt-message-specific-process-details) |
| [Get Receipt Process by Document UUID](actions/get-receipt-process-by-document-uuid.md) | `GET /receipts/process/document/:document_uuid` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#sent-receipt-message-specific-process-details) |
| [Get Received Receipt by UUID](actions/get-received-receipt-by-uuid.md) | `GET /receipts/received/:uuid` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#received-receipt-message) |
| [Get Sent Receipt by UUID](actions/get-sent-receipt-by-uuid.md) | `GET /receipts/sent/:uuid` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#receipt) |
| [Get Shared Document by UUID](actions/get-shared-document-by-uuid.md) | `GET /sharedoc/:document_uuid` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html) |
| [Get Shared Document Process](actions/get-shared-document-process.md) | `GET /sharedoc/process/:process_id` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#specific-sent-process-details) |
| [Get Wallet Address](actions/get-wallet-address.md) | `GET /wallet/address` | [docs](https://docs.commercio.network/app_developers/commercioapi-wallet.html#get-your-wallet-address-and-balance) |
| [Get Wallet Balance](actions/get-wallet-balance.md) | `GET /wallet/balance` | [docs](https://docs.commercio.network/app_developers/commercioapi-wallet.html#get-wallet-balance) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://docs.commercio.network/app_developers/commercioapi-introduction.html) |
| [List Receipt Processes](actions/list-receipt-processes.md) | `GET /receipts/process` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#sent-receipts-processes) |
| [List Received Documents](actions/list-received-documents.md) | `GET /sharedoc/received` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#received-sharedoc) |
| [List Received Receipts](actions/list-received-receipts.md) | `GET /receipts/received` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#received-receipt-message) |
| [List Sent Documents](actions/list-sent-documents.md) | `GET /sharedoc/sent` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#sent-sharedoc) |
| [List Sent Receipts](actions/list-sent-receipts.md) | `GET /receipts/sent` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#receipt) |
| [List Shared Document Processes](actions/list-shared-document-processes.md) | `GET /sharedoc/process` | [docs](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#sent-processes) |
| [List Wallet Transfer Processes](actions/list-wallet-transfer-processes.md) | `GET /wallet/transfers/process` | [docs](https://docs.commercio.network/app_developers/commercioapi-wallet.html#sent-token-process-list) |
| [Request SPID Session](actions/request-spid-session.md) | `POST /eKYC/spid` | [docs](https://docs.commercio.network/app_developers/commercioapi-ekyc.html#request-spid-session) |
| [Verify Credentials](actions/verify-credentials.md) | `GET /eKYC/:address` | [docs](https://docs.commercio.network/app_developers/commercioapi-ekyc.html#verify-credentials) |
