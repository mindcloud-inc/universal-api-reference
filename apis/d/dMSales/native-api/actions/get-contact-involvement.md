# Get Contact Involvement with DMSales

Retrieves contact involvement details from DMSales.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/contact-card/involvement`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [Get Contact Involvement](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base_key` | query | `string` | yes | Contact base key. |
| `date_from` | query | `date` | yes | Start date (YYYY-MM-DD). |
| `date_to` | query | `date` | yes | End date (YYYY-MM-DD). |
