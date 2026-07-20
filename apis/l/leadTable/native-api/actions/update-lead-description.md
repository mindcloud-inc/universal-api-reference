# Update lead description with LeadTable

## Endpoint

- **Method:** `PUT`
- **Path:** `/lead/{leadID}/description`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Update lead description](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadID` | path | `string` | yes | The lead whose description will be replaced. |
| `description` | body | `string` | yes | The new lead description. |
