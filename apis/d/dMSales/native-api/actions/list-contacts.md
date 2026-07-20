# List Contacts with DMSales

Retrieves contacts from DMSales.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/persons/list`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [List Contacts](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paid_leads` | query | `string` | no | Whether to display paid leads: true, false, or all. Accepted values: `0`, `1`, `2`. |
