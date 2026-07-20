# Create pairing config with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/pairing-config`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Create pairing config](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `string` | no | Config JSON string |
| `product_id` | body | `number` | yes | Id of the product to which you want to add the config |
