# Create Redirect Payment with iPaymu

Create a payment session that redirects the buyer to the iPaymu payment page.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Create Redirect Payment](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product[]` | body | `array<string>` | yes | Product name list. |
| `qty[]` | body | `array<number>` | yes | Product quantity list. |
| `price[]` | body | `array<number>` | yes | Product price list. |
| `description[]` | body | `array<string>` | yes | Product description list. |
| `notifyUrl` | body | `string` | yes | Callback URL for payment updates. |
| `referenceId` | body | `string` | yes | Merchant reference for the payment. |
