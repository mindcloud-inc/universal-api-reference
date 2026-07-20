# List Traffic with GoAffPro

Retrieves affiliate traffic data from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/traffic`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Traffic](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return traffic for this affiliate ID. |
| `fields[]` | query | `array<string>` | yes | Fields to include in returned traffic records. |
