# Create Transaction Event with Weberlo

Creates a transaction event in Weberlo.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/transaction`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Create Transaction Event](https://developers.weberlo.com/#tag/Event/paths/~1event~1transaction/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time` | body | `number` | yes | Transaction timestamp in milliseconds. |
| `transaction_id` | body | `string` | yes | Unique transaction identifier. |
| `transaction_type` | body | `string` | yes | Transaction event type. |
| `transaction_amount` | body | `number` | yes | Transaction amount. |
| `transaction_description` | body | `string` | yes | Transaction description. |
| `transaction_currency` | body | `string` | no | Currency code. |
| `email` | body | `string` | no | Visitor email address. |
| `first_name` | body | `string` | no | Visitor first name. |
| `last_name` | body | `string` | no | Visitor last name. |
| `name` | body | `string` | no | Visitor full name. |
| `session_id` | body | `string` | no | Session identifier. |
| `platform` | body | `string` | no | Commerce or source platform. |
| `platform_id` | body | `string` | no | Platform-specific identifier. |
| `country` | body | `string` | no | Country code or country value. |
| `phone` | body | `string` | no | Visitor phone number. |
| `ip_address` | body | `string` | no | Visitor IP address. |
| `utm_source` | body | `string` | no | UTM source. |
| `utm_medium` | body | `string` | no | UTM medium. |
| `utm_campaign` | body | `string` | no | UTM campaign. |
| `utm_content` | body | `string` | no | UTM content. |
| `fbclid` | body | `string` | no | Facebook click identifier. |
| `gclid` | body | `string` | no | Google click identifier. |
| `parent_id` | body | `string` | no | Parent event or transaction ID. |
