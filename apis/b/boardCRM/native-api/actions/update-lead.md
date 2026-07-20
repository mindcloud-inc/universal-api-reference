# Update Lead with BoardCRM

Updates an existing lead in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/update`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Update Lead](https://dev.boardcrm.io/public/0.1/methods/lead#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Lead ID. |
| `name` | body | `string` | no | Updated lead name. |
| `email` | body | `string` | no | Updated lead email. |
| `phone` | body | `string` | no | Updated lead phone number. |
