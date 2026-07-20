# Suggest Group Handle with Loomio

Retrieves a suggested group handle from Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/suggest_handle`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [Suggest Group Handle](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | The proposed group name. |
