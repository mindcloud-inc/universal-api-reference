# List Group Memberships with Loomio

Retrieves group memberships from Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/memberships`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Group Memberships](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/memberships_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | no | The Loomio group ID to list memberships for. |
