# Create Payment Tenant Company Configuration with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/configuration/tenant/company`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Tenant Company Configuration](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configurations[].configuration` | body | `object` | yes | Company configuration |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentProviderId` | body | `number` | yes | Payment provider (0 = Unknown, 1 = Finexio) |
| `configurations[]` | body | `array<object>` | yes | — |
| `configurations[].configuration.companyId` | body | `string` | yes | Company Id Format: `uuid`. |
| `configurations[].configuration.buyerId` | body | `string` | yes | Buyer identification |
| `configurations[].configuration.buyerName` | body | `string` | yes | Name of the buyer |
| `configurations[].configuration.bankAccountIdentifier` | body | `number` | yes | Last four digits of bank account identifier |
| `configurations[].configuration.startDate` | body | `date` | yes | Date for where payment processing should start Format: `date-time`. |
