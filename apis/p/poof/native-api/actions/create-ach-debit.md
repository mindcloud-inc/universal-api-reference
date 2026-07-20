# Create ACH Debit with Poof

Creates a new ACH debit in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v2/ach_debit`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Create ACH Debit](https://docs.poof.io/reference/ach-debit-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | ACH debit amount in USD. |
| `account_number` | body | `string` | yes | Bank account number. |
| `routing_number` | body | `string` | yes | Bank routing number. |
