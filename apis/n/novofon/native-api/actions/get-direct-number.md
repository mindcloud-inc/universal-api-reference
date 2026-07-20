# Get Direct Number with Novofon

Retrieves a direct number from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/direct_numbers/number/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get Direct Number](https://novofon.com/instructions/api/#direct_numbers_number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | Purchased direct number to inspect. |
| `type` | query | `string` | yes | Number type. Docs say `revenue` for free Moscow 495 numbers and `common` for regular numbers. |
