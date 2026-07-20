# Create Receipt with CommercioNetwork

Creates a receipt process in CommercioNetwork.

## Endpoint

- **Method:** `POST`
- **Path:** `/receipts`
- **Base URL:** `https://dev-api.commercio.app/v1`
- **Official documentation:** [Create Receipt](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#send-a-receipt-message-process)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_tx_hash` | body | `string` | yes | The transaction hash of the shared document. |
| `document_uuid` | body | `string` | yes | The UUID of the shared document. |
