# List Group Subgroups with Loomio

Retrieves subgroups from a Loomio group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:id/subgroups`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Group Subgroups](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | The Loomio group ID. |
