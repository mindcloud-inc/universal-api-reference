# Create Book Transfer with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/book`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Book Transfer](https://column.com/docs/api/#book-transfer/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount in cents of the book transfer. |
| `currency_code` | body | `string` | yes | ISO 4217 currency code for the transfer. |
| `sender_bank_account_id` | body | `string` | no | Sender bank account ID. Provide either Sender Bank Account ID or Sender Account Number ID. |
| `sender_account_number_id` | body | `string` | no | Specific sender account number ID. |
| `receiver_bank_account_id` | body | `string` | no | Receiver bank account ID. Provide either Receiver Bank Account ID or Receiver Account Number ID. |
| `receiver_account_number_id` | body | `string` | no | Specific receiver account number ID. |
| `description` | body | `string` | no | Description visible in account activity. |
| `hold` | body | `boolean` | no | Create the book transfer in hold state so it can be cleared or canceled later. |
