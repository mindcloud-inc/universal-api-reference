# List Orders with MailBluster

Retrieves a page of orders from MailBluster.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [List Orders](https://app.mailbluster.com/api-doc/orders/read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNo` | query | `number` | no | Page number to retrieve. |
| `perPage` | query | `number` | no | Number of orders to retrieve per page. |
