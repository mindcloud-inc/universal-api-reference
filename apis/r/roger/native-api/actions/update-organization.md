# Update Organization with Roger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organizations/:id`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Update Organization](https://developer.rogerroger.io/organizations)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Organization identifier. |
| `description` | body | `string` | yes | Updated organization description. |
