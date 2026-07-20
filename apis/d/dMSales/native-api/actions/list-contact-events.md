# List Contact Events with DMSales

Retrieves contact events from DMSales.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/contact-card/events`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [List Contact Events](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base_key` | query | `string` | yes | Contact base key. |
| `date_from` | query | `date` | no | Start date for event filtering (YYYY-MM-DD). |
| `date_to` | query | `date` | no | End date for event filtering (YYYY-MM-DD). |
