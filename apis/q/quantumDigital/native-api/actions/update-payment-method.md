# Update Payment Method with Quantum Digital

## Endpoint

- **Method:** `PUT`
- **Path:** `/devplatform/billing/:dashboardAccountId/paymentmethods`
- **Base URL:** `https://api.quantumdigital.com`
- **Official documentation:** [Update Payment Method](https://developer.quantumdigital.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billingAddress1` | body | `string` | yes | — |
| `billingAddress2` | body | `string` | no | — |
| `billingCity` | body | `string` | yes | — |
| `billingCountry` | body | `list` | yes | Accepted values: `Canada`, `United States`. |
| `billingPostalCode` | body | `string` | yes | — |
| `billingStateProvince` | body | `string` | yes | — |
| `creditCardNumber` | body | `string` | yes | — |
| `creditCardType` | body | `list` | yes | Accepted values: `American Express`, `Discover`, `Mastercard`, `Visa`. |
| `expMonth` | body | `string` | yes | — |
| `expYear` | body | `string` | yes | — |
| `nameOnCard` | body | `string` | yes | — |
