# Format Number with Seven

Retrieves formatted phone number details from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/format`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Format Number](https://docs.seven.io/en/rest-api/endpoints/lookup#format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | The number to be queried. Multiple numbers must be separated by commas. You can enter almost any format; the API formats the number automatically. |
