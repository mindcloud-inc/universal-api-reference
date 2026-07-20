# Update Multiple Records with Airtable

Updates multiple records in a specific Airtable table, or upserts them when enabled.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:baseId/:tableIdOrName`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [Update Multiple Records](https://airtable.com/developers/web/api/update-multiple-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `list<string>` | yes | — |
| `tableIdOrName` | path | `list<string>` | yes | — |
| `records[]` | body | `array<object>` | yes | Airtable records array (max 10). Each item must include an id and a fields object. |
| `records[].id` | body | `string` | no | Airtable record ID (rec...). Row number is not accepted. |
| `records[].fields` | body | `object` | yes | JSON object with field names as keys, e.g. {"name":"Updated"}. |
| `typecast` | body | `boolean` | no | — |
| `returnFieldsByFieldId` | body | `boolean` | no | — |
| `performUpsert` | body | `object` | no | — |
| `performUpsert.fieldsToMergeOn[]` | body | `array<string>` | no | — |
