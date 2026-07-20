# Create Shape with Aspose

Creates a new shape in a slide in Aspose.

## Endpoint

- **Method:** `POST`
- **Path:** `/slides/:name/slides/:slideIndex/shapes`
- **Base URL:** `https://api.aspose.cloud/v3.0`
- **Official documentation:** [Create Shape](https://docs.aspose.cloud/slides/add-a-shape-to-a-slide/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The presentation file name. |
| `slideIndex` | path | `number` | yes | The 1-based slide index. |
| `dto` | body | `object` | yes | The shape payload. |
