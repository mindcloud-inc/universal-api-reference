# Add Items to List with DataMerge

Adds companies or contacts to a DataMerge list.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/lists/:object_type/:list/add`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Add Items to List](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_type` | path | `string` | yes | List object type. |
| `list` | path | `string` | yes | List slug. |
| `domains[]` | body | `array<string>` | no | Company domains to add to a company list. |
| `contact_ids[]` | body | `array<string>` | no | Contact record IDs to add to a contact list. |
