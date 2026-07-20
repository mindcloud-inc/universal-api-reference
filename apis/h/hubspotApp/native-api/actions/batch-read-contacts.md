# Batch Read Contacts with HubSpot

Retrieves contacts from HubSpot in a batch.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/contacts/batch/read`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Read Contacts](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/batch/post-crm-v3-objects-contacts-batch-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | The list of contact identifiers to read. |
| `inputs[].id` | body | `string` | yes | A contact record ID or unique property value. |
| `properties[]` | body | `array<string>` | no | Contact properties to include in the response. |
| `propertiesWithHistory[]` | body | `array<string>` | no | Contact properties to return with value history. |
| `idProperty` | body | `string` | no | The unique property to use instead of the default record ID. |
