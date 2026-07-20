# List Related Messages with BulkSMS

Retrieves received messages related to a sent BulkSMS message.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:id/relatedReceivedMessages`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [List Related Messages](https://www.bulksms.com/developer/json/v1/#tag/message/GET/messages/{id}/relatedReceivedMessages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The sent message ID whose related received replies should be listed. |
