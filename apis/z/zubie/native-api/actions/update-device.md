# Update Device with Zubie

Updates an existing device in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/device/{key}`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Update Device](https://developer.zubie.com/reference/devices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Unique device key. |
| `subscription_status` | body | `string` | yes | Specify canceled to mark a device as Do Not Renew or active to restore renewal. |
