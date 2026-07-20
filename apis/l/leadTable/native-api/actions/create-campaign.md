# Create campaign with LeadTable

## Endpoint

- **Method:** `POST`
- **Path:** `/table/create`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Create campaign](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerID` | body | `string` | yes | The customer that will own the campaign. |
| `occupation` | body | `string` | yes | Campaign or table name. |
| `funnelLink` | body | `string` | no | Optional funnel link for the campaign. |
| `preQualify` | body | `boolean` | no | Whether leads should be pre-qualified. |
| `deleteLeads` | body | `boolean` | no | Whether existing leads should be deleted. |
| `tableAndProfileConfig[]` | body | `array<object>` | no | Optional configuration array for table and profile fields. |
| `overrideValues` | body | `object` | no | Optional object of override values. |
| `status[]` | body | `array<string>` | no | Optional list of statuses for the campaign. |
