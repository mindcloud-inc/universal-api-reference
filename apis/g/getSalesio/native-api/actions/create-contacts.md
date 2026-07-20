# Create Contacts with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/api/leads`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Create Contacts](https://api.getsales.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uuid` | body | `string` | yes | UUID of the list that will contain the created contacts. |
| `leads[]` | body | `array<object>` | yes | Array of contacts to create. Each contact may include LinkedIn ID, first name, last name, company name, email, and custom fields. |
