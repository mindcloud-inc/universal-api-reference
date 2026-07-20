# Create Transformation with Pabbly Hook

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/transformations`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Create Transformation](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Transformation name. |
| `code` | body | `string` | yes | Transformation JavaScript code. |
