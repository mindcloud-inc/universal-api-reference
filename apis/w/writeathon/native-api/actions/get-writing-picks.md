# Get Writing Picks with Writeathon

Retrieves writing picks from the current Writeathon account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/writing-pick`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Get Writing Picks](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | no | Optional writing-pick scope: all, page, or card. |
| `limit` | body | `number` | no | How many writing picks to return, from 1 to 10. |
