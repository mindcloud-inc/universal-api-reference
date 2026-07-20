# Upsert lead field with LeadTable

## Endpoint

- **Method:** `PUT`
- **Path:** `/lead/{leadID}`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Upsert lead field](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadID` | path | `string` | yes | The lead to update. |
| `question` | body | `string` | yes | The lead field name to create or update. |
| `answer` | body | `string` | yes | The value to store in the selected lead field. |
| `setVisibleInProfile` | body | `boolean` | no | Whether the field should be visible in the lead profile. |
