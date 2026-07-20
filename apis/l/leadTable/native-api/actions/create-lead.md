# Create lead with LeadTable

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/create`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Create lead](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignID` | body | `string` | yes | The campaign or table where the lead will be created. |
| `data[]` | body | `array<object>` | yes | Array of lead field objects to create. |
| `notifications` | body | `boolean` | no | Whether LeadTable should trigger notifications for the new lead. |
| `date` | body | `date` | no | Optional lead timestamp in ISO 8601 format. |
