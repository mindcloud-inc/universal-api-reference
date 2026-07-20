# Get Device Variable with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/:device_key/variables/:variable_key/`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Device Variable](https://docs.ubidots.com/reference/get-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_key` | path | `string` | yes | The device ID or API label. |
| `variable_key` | path | `string` | yes | The variable API label. |
