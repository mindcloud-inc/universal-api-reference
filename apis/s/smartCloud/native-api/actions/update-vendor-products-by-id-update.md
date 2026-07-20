# Update product with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/products/{id}/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update product](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `title` | body | `string` | no | Product title |
| `mcu` | body | `string` | no | Product microcontroller type |
| `type` | body | `string` | no | Product abbrevation type |
| `layout_id` | body | `number` | no | ID of a layout |
| `firmware_id` | body | `number` | no | ID of a firmware |
| `production_build_id` | body | `number` | no | ID of a production build (only for custom firmware) |
| `description` | body | `string` | no | Text description for product |
| `instruction` | body | `string` | no | Text instruction for product in markdown |
| `changelog` | body | `string` | no | Changelog for product version |
| `icon` | body | `string` | no | Path for uploaded icon witout STATIC_URL |
| `picture` | body | `string` | no | Path for uploaded picture witout STATIC_URL |
