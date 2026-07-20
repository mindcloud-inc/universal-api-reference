# List Calls with CallPage

Retrieves call history records from CallPage.

## Endpoint

- **Method:** `GET`
- **Path:** `https://core.callpage.io/api/v3/external/calls/history`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [List Calls](https://callpage.github.io/documentation-rest/#get-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_hidden` | query | `number` | no | Whether to include hidden calls. |
| `call_id` | query | `number<number>` | no | Filter by one or more call IDs. Send multiple values as a array. |
| `phone_number` | query | `string` | no | Filter by visitor phone number in E.164 format. |
| `user_ids` | query | `number<number>` | no | Filter by one or more user IDs. Send multiple values as a array. |
| `statuses` | query | `list<string>` | no | Filter by one or more call statuses. Accepted values: `cancelled`, `completed`, `failed`, `in-progress`, `manager-failed`, `new`, `ringing`, `scheduled`, `user-failed`. Send multiple values as a array. |
| `tag_ids` | query | `number<number>` | no | Filter by one or more tag IDs. Send multiple values as a array. |
| `date_from` | query | `number` | no | Start timestamp filter. |
| `date_to` | query | `number` | no | End timestamp filter. |
| `widget_ids` | query | `number<number>` | no | Filter by one or more widget IDs. Send multiple values as a array. |
| `url` | query | `string` | no | Filter by widget installation URL. |
| `incoming_number_ids` | query | `number<number>` | no | Filter by one or more incoming number IDs. Send multiple values as a array. |
