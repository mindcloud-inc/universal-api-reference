# Get List with Planning Center

Retrieves a list from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/lists/:id`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Get List](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | List ID |
| `include` | query | `string` | no | Include associated resources |
