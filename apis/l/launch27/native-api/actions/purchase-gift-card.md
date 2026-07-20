# Purchase Gift Card with Launch27

Creates a new gift card purchase in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `giftcard`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Purchase Gift Card](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient_name` | body | `string` | yes | Gift card recipient name. |
| `recipient_email` | body | `string` | yes | Gift card recipient email address. |
| `sender_name` | body | `string` | yes | Gift card sender name. |
| `sender_email` | body | `string` | yes | Gift card sender email address. |
| `message` | body | `string` | yes | Gift card message text. |
| `amount` | body | `number` | yes | Gift card amount. |
| `discount_code` | body | `string` | no | Optional gift card discount code. |
| `recaptcha_token` | body | `string` | no | Recaptcha token for gift card submission. |
| `fspay_payment_method_id` | body | `string` | no | FullSteam payment method ID for FSPay gift card purchases. |
