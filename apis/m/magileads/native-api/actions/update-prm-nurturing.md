# Update PRM Nurturing with Magileads

Updates an existing PRM nurturing in Magileads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/prm/nurturing/:nurturing_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Update PRM Nurturing](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The updated nurturing name. |
| `nurturing_id` | path | `number` | yes | The nurturing ID. |
| `filter` | body | `object` | no | The updated nurturing filter object. |
| `contact_list_ids[]` | body | `array<number>` | no | The updated contact list IDs. |
