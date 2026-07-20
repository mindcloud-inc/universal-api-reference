# Update Order with TrackMage

Updates an existing order in TrackMage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/{id}`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Update Order](https://docs.trackmage.com/docs/order/order.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource identifier |
| `subtotal` | body | `string` | no | The current subtotal price of the order in the store currency. Default value is **0** |
| `total` | body | `string` | no | The current total price of the order in the store currency. Default value is **0** |
| `currency` | body | `string` | no | A three-letter currency code. Default value is **USD** |
| `orderStatus.code` | body | `string` | no | A unique status code. This field is required. |
| `orderStatus.title` | body | `string` | no | A status name. This field is optional. |
| `orderStatus.description` | body | `string` | no | — |
| `email` | body | `string` | no | Customer email address. |
| `phoneNumber` | body | `string` | no | Customer phone number. |
| `shipments[]` | body | `array<string>` | no | List of [shipment](/docs/Shipment/shipment.html) references that belong to the order. |
| `shippingAddress.addressLine1` | body | `string` | no | The street address. This field is optional. |
| `shippingAddress.addressLine2` | body | `string` | no | An optional additional field for the street address. This field is optional. |
| `shippingAddress.city` | body | `string` | no | The city, town, or village. This field is optional. |
| `shippingAddress.company` | body | `string` | no | The company of the person associated with the address. This field is optional. |
| `shippingAddress.country` | body | `string` | no | The name of the country. This field is optional. |
| `shippingAddress.countryIso2` | body | `string` | no | The two-letter country code. This field is optional. |
| `shippingAddress.firstName` | body | `string` | no | The first name of the person associated with the address. This field is optional. |
| `shippingAddress.lastName` | body | `string` | no | The last name of the person associated with the address. This field is optional. |
| `shippingAddress.postcode` | body | `string` | no | The postal code (zip, postcode, Eircode, …). This field is optional. |
| `shippingAddress.state` | body | `string` | no | The name of the region (province, state, prefecture, …). This field is optional. |
| `billingAddress.addressLine1` | body | `string` | no | The street address. This field is optional. |
| `billingAddress.addressLine2` | body | `string` | no | An optional additional field for the street address. This field is optional. |
| `billingAddress.city` | body | `string` | no | The city, town, or village. This field is optional. |
| `billingAddress.company` | body | `string` | no | The company of the person associated with the address. This field is optional. |
| `billingAddress.country` | body | `string` | no | The name of the country. This field is optional. |
| `billingAddress.countryIso2` | body | `string` | no | The two-letter country code. This field is optional. |
| `billingAddress.firstName` | body | `string` | no | The first name of the person associated with the address. This field is optional. |
| `billingAddress.lastName` | body | `string` | no | The last name of the person associated with the address. This field is optional. |
| `billingAddress.postcode` | body | `string` | no | The postal code (zip, postcode, Eircode, …). This field is optional. |
| `billingAddress.state` | body | `string` | no | The name of the region (province, state, prefecture, …). This field is optional. |
