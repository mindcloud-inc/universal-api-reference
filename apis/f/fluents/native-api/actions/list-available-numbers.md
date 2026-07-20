# List Available Numbers with Fluents

Retrieves available phone numbers from Fluents.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/available`
- **Base URL:** `https://api.fluents.ai/v1`
- **Official documentation:** [List Available Numbers](https://docs.fluents.ai/api-reference/numbers/list-available-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | yes | Maximum number of available numbers to return. |
| `telephony_provider` | query | `string` | yes | Telephony provider to search, for example twilio. |
| `telephony_account_connection` | query | `string` | yes | Fluents telephony account connection ID to source numbers from. |
| `filters` | query | `string` | yes | JSON-encoded Fluents filters string. |
