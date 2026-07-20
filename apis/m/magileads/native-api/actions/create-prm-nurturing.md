# Create PRM Nurturing with Magileads

Creates a new PRM nurturing in Magileads.

## Endpoint

- **Method:** `POST`
- **Path:** `/prm/nurturing`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Create PRM Nurturing](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The nurturing name. |
| `filter` | body | `object` | yes | The nurturing filter object. |
| `contact_list_ids[]` | body | `array<number>` | yes | The contact list IDs to include in the nurturing. |
