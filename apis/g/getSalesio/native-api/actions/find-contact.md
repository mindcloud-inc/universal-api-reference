# Find Contact with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/api/leads/lookup-one`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Find Contact](https://api.getsales.io/api/openapi/contacts/findonecontact.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkedin_id` | body | `string` | no | LinkedIn URL, handle, or ID used to identify the contact. |
| `email` | body | `string` | no | Email address used to identify the contact. |
| `name` | body | `string` | no | Contact name used with company name for lookup. |
| `company_name` | body | `string` | no | Company name used with contact name for lookup. |
| `disable_aggregation` | body | `boolean` | no | When true, disables contact data aggregation. |
