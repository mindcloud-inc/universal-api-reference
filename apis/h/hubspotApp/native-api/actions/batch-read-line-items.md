# Batch Read Line Items with HubSpot

Retrieves line items from HubSpot in a batch.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/line_items/batch/read`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Read Line Items](https://developers.hubspot.com/docs/api-reference/crm-line-items-v3/batch/post-crm-v3-objects-line_items-batch-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | The line items to batch read. |
| `inputs[].id` | body | `string` | no | The line item ID to batch read. |
| `properties[]` | body | `array<string>` | no | Properties to include in each returned line item. |
| `propertiesWithHistory[]` | body | `array<string>` | no | Properties to include with history values in each returned line item. |
| `idProperty` | query | `string` | no | The unique property to use instead of the default record ID. |
| `archived` | query | `boolean` | no | Whether to read archived line items. |
