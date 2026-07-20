# <img src="https://images.mindcloud.co/apps/icons/45789950_1781641901371.png" alt="CommercioNetwork logo" width="28" height="28"> CommercioNetwork: Universal API

CommercioNetwork is a public documents blockchain and tokenization platform with wallet, DID, and document-ledger APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/commercioNetwork/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://commercio.network/
- **Vendor API docs:** https://docs.commercio.network/app_developers/commercioapi-introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Wallet Address](actions/get-wallet-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-wallet-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Receipt](actions/create-receipt.md) | POST | Creates a receipt process in CommercioNetwork. |
| [Create Shared Document Process](actions/create-shared-document-process.md) | POST | Creates a shared document process in CommercioNetwork. |
| [Get Receipt Process](actions/get-receipt-process.md) | GET | Retrieves a receipt process from CommercioNetwork. |
| [Get Receipt Process by Document UUID](actions/get-receipt-process-by-document-uuid.md) | GET | Retrieves a receipt process from CommercioNetwork by document UUID. |
| [Get Received Receipt by UUID](actions/get-received-receipt-by-uuid.md) | GET | Retrieves a received receipt from CommercioNetwork by UUID. |
| [Get Sent Receipt by UUID](actions/get-sent-receipt-by-uuid.md) | GET | Retrieves a sent receipt from CommercioNetwork by UUID. |
| [Get Shared Document by UUID](actions/get-shared-document-by-uuid.md) | GET | Retrieves a shared document from CommercioNetwork by UUID. |
| [Get Shared Document Process](actions/get-shared-document-process.md) | GET | Retrieves a shared document process from CommercioNetwork. |
| [Get Wallet Address](actions/get-wallet-address.md) | GET | Retrieves your wallet address from CommercioNetwork. |
| [Get Wallet Balance](actions/get-wallet-balance.md) | GET | Retrieves your wallet balance from CommercioNetwork. |
| [Health Check](actions/health-check.md) | GET | Retrieves the CommercioNetwork API health status. |
| [List Receipt Processes](actions/list-receipt-processes.md) | GET | Retrieves receipt processes from CommercioNetwork. |
| [List Received Documents](actions/list-received-documents.md) | GET | Retrieves received shared documents from CommercioNetwork. |
| [List Received Receipts](actions/list-received-receipts.md) | GET | Retrieves received receipts from CommercioNetwork. |
| [List Sent Documents](actions/list-sent-documents.md) | GET | Retrieves sent shared documents from CommercioNetwork. |
| [List Sent Receipts](actions/list-sent-receipts.md) | GET | Retrieves sent receipts from CommercioNetwork. |
| [List Shared Document Processes](actions/list-shared-document-processes.md) | GET | Retrieves shared document processes from CommercioNetwork. |
| [List Wallet Transfer Processes](actions/list-wallet-transfer-processes.md) | GET | Retrieves wallet transfer processes from CommercioNetwork. |
| [Request SPID Session](actions/request-spid-session.md) | POST | Creates a SPID session in CommercioNetwork. |
| [Verify Credentials](actions/verify-credentials.md) | GET | Retrieves credential verification details from CommercioNetwork. |

