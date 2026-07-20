# Check Balance with Poof

Retrieves wallet balance details from Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `/balance`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Check Balance](https://docs.poof.io/reference/check_balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crypto` | body | `string` | yes | Crypto asset code. |
