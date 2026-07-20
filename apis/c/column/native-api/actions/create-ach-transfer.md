# Create ACH Transfer with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/ach`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create ACH Transfer](https://column.com/docs/api/#ach-transfer/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount in cents of the ACH transfer. |
| `currency_code` | body | `string` | yes | ISO 4217 currency code for the transfer. |
| `bank_account_id` | body | `string` | no | Column bank account ID to send the transfer from. Provide either Bank Account ID or Account Number ID. |
| `account_number_id` | body | `string` | no | Specific Column account number ID to send the transfer from. |
| `counterparty_id` | body | `string` | yes | Counterparty ID that will receive the transfer. |
| `type` | body | `string` | yes | ACH transfer direction: CREDIT or DEBIT. |
| `entry_class_code` | body | `string` | yes | ACH Standard Entry Class code. |
| `description` | body | `string` | no | Internal description visible in your platform. |
| `effective_date` | body | `date` | no | Effective date in YYYY-MM-DD format. |
| `same_day` | body | `boolean` | no | Whether to submit the ACH transfer as same-day ACH. |
