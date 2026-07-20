# List Channel Threads with Zoho Cliq

Retrieves threads from a Zoho Cliq channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/threads`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Channel Threads](https://www.zoho.com/cliq/help/restapi/v2/#get-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The ID of the channel whose threads should be retrieved. |
| `state` | query | `string` | no | Filter threads by follow state: followed, not_followed, or all. |
| `type` | query | `string` | no | Filter threads by status, such as open or closed. |
| `next_token` | body | `string` | no | Use the next token from a previous response to retrieve the next thread page. |
| `limit` | body | `number` | no | The maximum number of threads to return. |
