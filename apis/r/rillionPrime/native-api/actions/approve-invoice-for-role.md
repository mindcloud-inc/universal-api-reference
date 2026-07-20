# Approve Invoice For Role with Rillion Prime

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/approve/:invoiceId`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Approve Invoice For Role](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceId` | path | `number` | yes | Path value for InvoiceId. |
| `quickSign` | query | `boolean` | no | Set to true to use quick-sign behavior when supported. |
| `signingRole` | body | `string` | yes | Request body value for SigningRole. |
| `invoiceAccountCoding` | body | `array` | yes | Request body value for InvoiceAccountCoding. |
| `signingRole` | body | `string` | yes | Request body value for SigningRole. |
| `invoiceAccountCoding` | body | `array` | yes | Request body value for InvoiceAccountCoding. |
| `signingRole` | body | `string` | yes | Request body value for SigningRole. |
| `invoiceAccountCoding` | body | `array` | yes | Request body value for InvoiceAccountCoding. |
