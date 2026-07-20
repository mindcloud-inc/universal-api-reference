# Update Group with ActiveTrail

Updates an existing group in ActiveTrail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:id`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Update Group](https://webapi.mymarketing.co.il/api/docs/and/Api/PUT-api-groups-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Group id. Can be found using the account groups endpoint or in the UI. |
| `name` | body | `string` | no | Name of the group. |
