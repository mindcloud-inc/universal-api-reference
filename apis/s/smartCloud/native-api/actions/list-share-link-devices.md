# List shared devices with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/share-link-devices`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List shared devices](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | query | `string` | no |
| `share_id` | query | `number` | no |
| `owner_id` | query | `number` | no |
| `receiver_id` | query | `number` | no |
| `device_id` | query | `string` | no |
| `is_hidden` | query | `boolean` | no |
