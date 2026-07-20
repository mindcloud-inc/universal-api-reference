# Upsert Customers with Retently

Creates or updates customers in Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Upsert Customers](https://www.retently.com/api/#api-create-or-update-customers-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscribers[]` | body | `array<string>` | yes | An array of customers |
| `subscribers[].email` | body | `string` | yes | Email address |
| `subscribers[].firstName` | body | `string` | no | First name |
| `subscribers[].lastName` | body | `string` | no | Last name |
| `subscribers[].company` | body | `string` | no | Company name |
| `subscribers[].tags[]` | body | `array<string>` | no | An array of tags. Example: [âfooâ, âbarâ, âbazâ] |
| `subscribers[].properties[]` | body | `array<object>` | no | Customer properties to create or update. |
| `subscribers[].properties[].label` | body | `string` | yes | Property label |
| `subscribers[].properties[].type` | body | `string` | yes | Property type |
| `subscribers[].properties[].value` | body | `string` | yes | Property value |
