# Create Partial Payment – Stripe to Aspire Sync with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `PartialPayments`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Partial Payment – Stripe to Aspire Sync](https://guide.youraspire.com/v1-api/apidocs/en/partialpayments-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Amount` | body | `number` | yes | — |
| `BillingCompany` | body | `string` | no | Billing Company and/or Billing Contact are required. Maximum length: 100. |
| `BillingContact` | body | `string` | no | Billing Company and/or Billing Contact are required. Maximum length: 250. |
| `BranchName` | body | `string` | no | — |
| `InvoiceNumber` | body | `number` | no | — |
| `PaymentDate` | body | `string` | yes | — |
| `PaymentMethod` | body | `list<string>` | yes | — |
| `PaymentNote` | body | `string` | no | — |
| `PaymentReference` | body | `string` | yes | — |
