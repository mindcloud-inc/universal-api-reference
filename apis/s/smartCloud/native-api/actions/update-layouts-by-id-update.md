# Update layout with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/layouts/{id}/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update layout](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `title` | body | `string` | no | Title for alyout |
| `schema` | body | `string` | no | Schema JSON string |
