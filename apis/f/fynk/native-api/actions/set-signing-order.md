# Set Signing Order with fynk

Updates signing order for a document in fynk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document/signatories/order`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Set Signing Order](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `signing_order` | body | `list<string>` | yes | The UUIDs of the document signatories in signing order. |
