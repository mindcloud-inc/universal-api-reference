# Update Transformation with Pabbly Hook

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/transformations/:transformationId`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Update Transformation](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transformationId` | path | `string` | yes | Transformation ID to update. |
| `name` | body | `string` | no | Transformation name. |
| `code` | body | `string` | no | Transformation JavaScript code. |
