# Retrieve Messages with BulkSMS

Retrieves sent or received messages from BulkSMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Retrieve Messages](https://www.bulksms.com/developer/json/v1/#tag/message/GET/messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | URL-encoded BulkSMS message filter clauses, such as type=SENT or status.type=DELIVERED. |
| `sortOrder` | query | `list` | no | Message sort order. BulkSMS supports ASC or DESC. Accepted values: `0`, `1`. |
