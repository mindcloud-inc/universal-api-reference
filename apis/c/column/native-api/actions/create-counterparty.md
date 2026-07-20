# Create Counterparty with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/counterparties`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Counterparty](https://column.com/docs/api/#counterparty/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routing_number` | body | `string` | yes | The routing number of the bank. |
| `account_number` | body | `string` | yes | The account number of the bank account. |
| `account_type` | body | `list` | no | The type of the account number. Can be checking or savings. Accepted values: `0`, `1`. |
| `routing_number_type` | body | `list` | no | The type of the routing number. Can be aba or bic. Accepted values: `0`, `1`. |
| `description` | body | `string` | no | Description of the counterparty visible only in your platform. |
