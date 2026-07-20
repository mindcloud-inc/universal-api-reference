# Cancel Document with Xodo Sign

Cancels an existing document in Xodo Sign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Cancel Document](https://eversign.com/api/documentation/methods#cancel-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document. |
| `document_hash` | query | `string` | yes | The unique document hash to cancel. |
