# Create Contact with SalesapCRM

Creates a contact in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Contact](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for a contact, including type, attributes, and optional relationships. |
