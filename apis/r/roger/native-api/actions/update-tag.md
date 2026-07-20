# Update Tag with Roger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tags/:id`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Update Tag](https://developer.rogerroger.io/global/tags)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Tag identifier. |
| `description` | body | `string` | yes | Updated tag description. |
