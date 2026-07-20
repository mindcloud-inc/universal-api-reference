# Get Message with Cody

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:id`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Get Message](https://developers.meetcody.ai/operation/operation-get-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id of the message. |
| `includes` | query | `list<string>` | no | Extra message attributes to include in the response. Accepted values: `sources`, `usage`. |
