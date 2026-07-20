# Get Recent Cards with Writeathon

Retrieves recently updated cards from Writeathon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/{userId}/cards/recent`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Get Recent Cards](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_date_title` | query | `boolean` | no | Exclude system-generated date titles from the recent cards list. |
| `space` | query | `string` | no | Optional Writeathon space ID. Leave blank to use the default space. |
