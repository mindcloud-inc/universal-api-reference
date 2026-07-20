# List Rewards with GoAffPro

Retrieves a list of affiliate rewards from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/rewards`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Rewards](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return rewards for this affiliate ID. |
| `fields[]` | query | `array<string>` | yes | Fields to include in returned rewards. |
| `status` | query | `string` | no | Only return rewards with this status. |
| `type` | query | `string` | no | Only return rewards with this type. |
