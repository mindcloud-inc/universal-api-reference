# Get Receipt Process by Document UUID with CommercioNetwork

Retrieves a receipt process from CommercioNetwork by document UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/receipts/process/document/:document_uuid`
- **Base URL:** `https://dev-api.commercio.app/v1`
- **Official documentation:** [Get Receipt Process by Document UUID](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#sent-receipt-message-specific-process-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_uuid` | path | `string` | yes | The shared document UUID. |
