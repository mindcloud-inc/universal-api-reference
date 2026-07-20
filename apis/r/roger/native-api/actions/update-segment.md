# Update Segment with Roger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/segments/:id`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Update Segment](https://developer.rogerroger.io/lists)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Segment identifier. |
| `title` | body | `string` | yes | Updated segment title. |
