# Get lead with LeadTable

## Endpoint

- **Method:** `GET`
- **Path:** `/lead/{leadID}`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Get lead](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadID` | path | `string` | yes | The lead to retrieve. |
| `plainDescription` | query | `boolean` | no | Return a plain-text description instead of HTML when supported. |
