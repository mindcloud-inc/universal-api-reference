# List Group Documents with Loomio

Retrieves documents from a Loomio group.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/for_group`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Group Documents](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/documents_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | no | The Loomio group ID to list documents for. |
