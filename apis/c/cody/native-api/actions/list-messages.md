# List Messages with Cody

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [List Messages](https://developers.meetcody.ai/operation/operation-list-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | query | `string` | no | Id of the conversation to filter the list of messages to only that conversation. |
| `includes` | query | `list<string>` | no | Extra message attributes to include in the response. Accepted values: `sources`, `usage`. |
