# Create Annotation with Mendeley

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Create Annotation](https://dev.mendeley.com/methods/#creating-an-annotation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-annotation.1+json` |
| `Content-Type` | `application/vnd.mendeley-annotation.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | body | `string` | yes | ID of the document the annotation belongs to. |
| `filehash` | body | `string` | yes | filehash of the file the annotation belongs to. |
| `positions[]` | body | `array<object>` | yes | Annotation positions array as defined by the Mendeley API. |
| `text` | body | `string` | yes | Annotation text content. |
