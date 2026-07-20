# List Recurring Documents with Quaderno

Retrieves recurring billing documents from Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [List Recurring Documents](https://developers.quaderno.io/api/#tag/Recurring-Documents/operation/listRecurrings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search text to filter recurring documents. |
| `date` | query | `date` | no | Date filter for recurring documents. |
| `state` | query | `string` | no | State selector for recurring documents. |
| `contact` | query | `number` | no | Contact ID selector for recurring documents. |
