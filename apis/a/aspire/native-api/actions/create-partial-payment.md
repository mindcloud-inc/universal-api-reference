# Create Partial Payment with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `PartialPayments`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Partial Payment](https://guide.youraspire.com/v1-api/apidocs/en/partialpayments-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | — |
| `BillingCompany` | body | `string` | no | Billing Company and/or Billing Contact are required. Maximum length: 100. |
| `billingContact` | body | `string` | no | Billing Company and/or Billing Contact are required. Maximum length: 250. |
| `branchName` | body | `string` | no | — |
| `invoiceNumber` | body | `number` | no | — |
| `paymentDate` | body | `string` | yes | — |
| `paymentMethod` | body | `list<string>` | yes | — |
| `paymentNote` | body | `string` | no | — |
| `paymentReference` | body | `string` | yes | — |
