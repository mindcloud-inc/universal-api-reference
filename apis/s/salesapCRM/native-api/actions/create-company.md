# Create Company with SalesapCRM

Creates a company in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Company](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for a company, including type, attributes, and optional relationships. |
