# List Conversation Replies with SparrowDesk

Retrieves conversation replies from SparrowDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/{{id}}/replies`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [List Conversation Replies](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/replies/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SparrowDesk conversation ID. |
