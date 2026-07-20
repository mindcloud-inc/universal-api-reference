# Group Customers with ChargeDesk

Retrieves grouped customers from ChargeDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/grouped`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Group Customers](https://chargedesk.com/api-docs#customers-grouped)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Text to find matching customers and charges by name, email, username, phone, or last 4 card digits. |
