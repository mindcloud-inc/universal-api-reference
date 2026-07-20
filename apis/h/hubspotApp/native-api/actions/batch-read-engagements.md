# Batch Read Engagements with HubSpot

Retrieves engagement records from HubSpot in a batch.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/:engagementType/batch/read`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Read Engagements](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/batch/post-crm-v3-objects-objectType-batch-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engagementType` | path | `list` | yes | The CRM activity object type to batch read, such as notes, tasks, calls, emails, or meetings. Accepted values: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. |
| `inputs[]` | body | `array<object>` | yes | The records to batch read. |
| `inputs[].id` | body | `string` | yes | The record ID to batch read. |
| `properties[]` | body | `array<string>` | no | Properties to include in each returned activity record. |
| `propertiesWithHistory[]` | body | `array<string>` | no | Properties to include with history values in each returned activity record. |
| `idProperty` | query | `string` | no | The unique property to use instead of the default record ID. |
| `archived` | query | `boolean` | no | Whether to read archived records. |
