# Update Preference with Mercado Pago

Updates an existing checkout preference in Mercado Pago.

## Endpoint

- **Method:** `PUT`
- **Path:** `/checkout/preferences/{id}`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Update Preference](https://www.mercadopago.com.ar/developers/en/reference/preferences/_checkout_preferences_id/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `items[]` | body | `array<object>` | no | — |
| `items[].title` | body | `string` | no | — |
| `items[].quantity` | body | `number` | no | — |
| `items[].unit_price` | body | `number` | no | — |
| `items[].currency_id` | body | `string` | no | — |
| `payer` | body | `object` | no | — |
| `payer.email` | body | `string` | no | — |
| `payer.first_name` | body | `string` | no | — |
| `payer.last_name` | body | `string` | no | — |
| `payment_methods` | body | `object` | no | — |
| `payment_methods.installments` | body | `number` | no | — |
| `payment_methods.default_payment_method_id` | body | `string` | no | — |
| `payment_methods.default_installments` | body | `number` | no | — |
| `payment_methods.default_payment_type_id` | body | `string` | no | — |
| `payment_methods.excluded_payment_methods[]` | body | `array<object>` | no | — |
| `payment_methods.excluded_payment_methods[].id` | body | `string` | no | — |
| `payment_methods.excluded_payment_types[]` | body | `array<object>` | no | — |
| `payment_methods.excluded_payment_types[].id` | body | `string` | no | — |
| `back_urls` | body | `object` | no | — |
| `back_urls.success` | body | `string` | no | — |
| `back_urls.pending` | body | `string` | no | — |
| `back_urls.failure` | body | `string` | no | — |
| `notification_url` | body | `string` | no | Use an HTTPS callback URL. |
| `external_reference` | body | `string` | no | — |
| `auto_return` | body | `string` | no | — |
| `binary_mode` | body | `boolean` | no | — |
| `expires` | body | `boolean` | no | — |
