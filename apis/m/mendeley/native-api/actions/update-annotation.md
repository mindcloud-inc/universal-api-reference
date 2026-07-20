# Update Annotation with Mendeley

## Endpoint

- **Method:** `PATCH`
- **Path:** `/annotations/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Update Annotation](https://dev.mendeley.com/methods/#updating-an-annotation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-annotation.1+json` |
| `Content-Type` | `application/vnd.mendeley-annotation.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the annotation. |
| `text` | body | `string` | yes | Updated annotation text content. |
