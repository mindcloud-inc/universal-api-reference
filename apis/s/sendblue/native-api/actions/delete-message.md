# Delete Message with Sendblue

Soft deletes a message from Sendblue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/message/:message_handle`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Delete Message](https://docs.sendblue.com/api-v2/messages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_handle` | path | `string` | yes | Message handle to delete. |
