# Create Wire Transfer with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/wire`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Wire Transfer](https://column.com/docs/api/#wire-transfer/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount in cents of the wire transfer. |
| `currency_code` | body | `string` | yes | ISO 4217 currency code for the transfer. |
| `bank_account_id` | body | `string` | no | Bank account ID to send the wire from. Provide either Bank Account ID or Account Number ID. |
| `account_number_id` | body | `string` | no | Specific account number ID to send the wire from. |
| `counterparty_id` | body | `string` | yes | Counterparty ID that will receive the wire. The counterparty must have wire details attached. |
| `description` | body | `string` | no | Description transmitted to the beneficiary bank statement. |
