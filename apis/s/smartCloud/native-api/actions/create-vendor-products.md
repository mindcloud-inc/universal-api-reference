# Create Product with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/products`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Create Product](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Product title |
| `mcu` | body | `string` | yes | Product microcontroller type |
| `layout_id` | body | `number` | no | ID of a layout |
| `firmware_id` | body | `number` | no | ID of a firmware |
| `description` | body | `string` | no | Text description for product |
| `instruction` | body | `string` | no | Text instruction for product in markdown |
| `icon` | body | `string` | no | Path for uploaded icon witout STATIC_URL |
| `picture` | body | `string` | no | Path for uploaded picture witout STATIC_URL |
