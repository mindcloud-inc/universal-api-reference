# Delete Customers with Retently

Deletes existing customer records from Retently.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/customers`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Delete Customers](https://www.retently.com/api/#api-delete-customers-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscribers[]` | body | `array<string>` | yes | An array of subscriber emails |
| `subscribers[].email` | body | `string` | yes | Email address |
