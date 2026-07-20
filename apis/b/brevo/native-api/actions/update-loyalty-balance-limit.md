# Update Loyalty Balance Limit with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits/:blid`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Loyalty Balance Limit](https://developers.brevo.com/reference/updatebalancelimit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `bdid` | path | `string` | yes |
| `blid` | path | `string` | yes |
| `pid` | path | `string` | yes |
