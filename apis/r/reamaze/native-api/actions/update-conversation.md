# Update Conversation with Reamaze

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:slug`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Update Conversation](https://www.reamaze.com/api/put_conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Path parameter for slug. |
| `conversation` | body | `object` | no | Body payload field documented on https://www.reamaze.com/api/put_conversations. |
