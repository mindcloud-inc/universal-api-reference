# Create customer with LeadTable

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/create`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Create customer](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Customer name. |
| `description` | body | `string` | no | Optional customer description. |
