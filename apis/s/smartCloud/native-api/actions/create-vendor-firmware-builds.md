# Create firmware build with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmware-builds`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Create firmware build](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Type of a build |
| `product_version_id` | body | `number` | yes | ID of product version |
| `wifi_name` | body | `string` | no | Name (ssid) of users wifi AP |
| `wifi_password` | body | `string` | no | Password to users wifi AP |
