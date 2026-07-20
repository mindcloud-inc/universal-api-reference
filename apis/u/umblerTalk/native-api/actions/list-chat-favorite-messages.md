# List Chat Favorite Messages with Umbler Talk

Retrieves a chat's favorite messages from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/[:id]/favorite-messages/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Chat Favorite Messages](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The chat ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
