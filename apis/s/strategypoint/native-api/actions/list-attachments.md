# List Attachments with Strategypoint

Retrieves attachments from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/attachments`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Attachments](https://developer.clearpointstrategy.com/reference/listattachments-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of attachments to return. |
| `object` | query | `string` | no | Filter attachments by related object type. |
| `objectId` | query | `number` | no | Filter attachments by related object identifier. |
| `search` | query | `string` | no | Search text to match attachment names or metadata. |
| `start` | query | `number` | no | Offset into the attachment result set. |
