# Show Message with BulkSMS

Retrieves a message from BulkSMS by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:id`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Show Message](https://www.bulksms.com/developer/json/v1/#tag/message/GET/messages/{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The BulkSMS message ID to retrieve. |
