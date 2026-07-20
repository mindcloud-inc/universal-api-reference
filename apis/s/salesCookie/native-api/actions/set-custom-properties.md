# Set Custom Properties with Sales Cookie

Replaces custom properties on a Sales Cookie entity.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/SetCustomProperties`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Set Custom Properties](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-retrieve-or-set-custom-variables)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | System user, team, or plan ID. |
| `propertiesJson` | body | `string` | yes | JSON array string of custom properties to replace on the target entity. |
