# List Guest Memberships with Zenoti

## Endpoint

- **Method:** `GET`
- **Path:** `guests/:guestId/memberships`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [List Guest Memberships](https://docs.zenoti.com/reference/list-all-memberships-of-a-guest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `guestId` | path | `string` | yes |
| `center_id` | query | `list` | no |
