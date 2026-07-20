# List Webhooks with Grist

Finds webhooks in a Grist document.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/webhooks`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [List Webhooks](https://support.getgrist.com/api/#tag/webhooks/operation/listWebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
