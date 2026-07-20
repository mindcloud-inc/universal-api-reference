# Create Order with IgnitePost

Creates a new order in IgnitePost.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://dashboard.ignitepost.com/api/v1`
- **Official documentation:** [Create Order](https://dashboard.ignitepost.com/api-documentation#create-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `font` | body | `string` | yes | IgnitePOST font key from the List Fonts action. |
| `message` | body | `string` | yes | Handwritten message content, up to 450 characters. Maximum length: 450. |
| `image` | body | `string` | yes | Front image key from List Default Images or a public image URL. |
| `image_inside` | body | `string` | no | A stock image key or image URL for the card interior. |
| `image_backside` | body | `string` | no | A stock image key or image URL for the card back. |
| `insert` | body | `string` | no | An optional IgnitePOST insert key, such as a gift card insert. |
| `recipient_name` | body | `string` | no | Recipient full name. |
| `recipient_email` | body | `string` | no | Recipient email address for delivery notifications. |
| `recipient_company_name` | body | `string` | no | Recipient company name for business deliveries. |
| `recipient_address_one` | body | `string` | yes | Recipient street address line 1. |
| `recipient_address_two` | body | `string` | no | Recipient street address line 2, such as a suite or apartment. |
| `recipient_city` | body | `string` | yes | Recipient city. |
| `recipient_state` | body | `string` | yes | Recipient state or region code. |
| `recipient_zip` | body | `string` | yes | Recipient ZIP or postal code. |
| `sender_name` | body | `string` | no | Sender name shown on the card. |
| `sender_address_one` | body | `string` | no | Sender street address line 1. |
| `sender_address_two` | body | `string` | no | Sender street address line 2, such as a suite or apartment. |
| `sender_city` | body | `string` | no | Sender city. |
| `sender_state` | body | `string` | no | Sender state or region code. |
| `sender_zip` | body | `string` | no | Sender ZIP or postal code. |
| `send_on` | body | `date` | no | Schedule the order for a future send date in YYYY-MM-DD format. |
| `letter_template_id` | body | `number` | no | Letter template ID from the List Letter Templates action. |
| `uid` | body | `string` | no | Your external unique identifier for the order. |
| `metadata` | body | `object` | no | Object of key-value metadata to attach to the order. |
