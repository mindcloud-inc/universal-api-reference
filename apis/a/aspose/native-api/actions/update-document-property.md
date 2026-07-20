# Update Document Property with Aspose

Updates a document property in a presentation in Aspose.

## Endpoint

- **Method:** `PUT`
- **Path:** `/slides/:name/documentproperties/:propertyName`
- **Base URL:** `https://api.aspose.cloud/v3.0`
- **Official documentation:** [Update Document Property](https://docs.aspose.cloud/slides/update-document-properties/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The presentation file name. |
| `propertyName` | path | `string` | yes | The document property name. |
| `property` | body | `object` | yes | The document property payload. |
