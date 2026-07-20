# Batch Read Notes with HubSpot

Retrieves notes from HubSpot in a batch.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/notes/batch/read`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Read Notes](https://developers.hubspot.com/docs/api-reference/crm-notes-v3/batch/post-crm-v3-objects-notes-batch-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | Note IDs or unique-property values to read. |
| `inputs[].id` | body | `string` | yes | The note ID or unique-property value for one requested note. |
| `properties[]` | body | `array<string>` | no | Properties to return for each note. |
| `propertiesWithHistory[]` | body | `array<string>` | no | Properties to return with version history. |
| `idProperty` | body | `string` | no | Unique property name to use instead of the record ID. |
| `archived` | query | `boolean` | no | Whether to return archived notes only. |
