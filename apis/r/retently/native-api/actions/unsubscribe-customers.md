# Unsubscribe Customers with Retently

Unsubscribes customers from surveys in Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers/unsubscribe`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Unsubscribe Customers](https://www.retently.com/api/#api-unsubscribe-customers-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Opt out message |
| `subscribers[]` | body | `array<string>` | yes | An array of subscriber emails |
| `subscribers[].email` | body | `string` | yes | Email address |
