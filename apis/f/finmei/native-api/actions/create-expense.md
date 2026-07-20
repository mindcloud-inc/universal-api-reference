# Create Expense with Finmei

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses`
- **Base URL:** `https://app.finmei.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | yes | Expense currency code. |
| `date` | body | `date` | yes | Expense date. |
| `file` | body | `file` | yes | Expense file upload. |
| `seller` | body | `string` | yes | Expense seller name. |
| `total` | body | `number` | yes | Expense total amount. |
