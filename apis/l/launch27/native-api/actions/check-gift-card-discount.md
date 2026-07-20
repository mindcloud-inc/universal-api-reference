# Check Gift Card Discount with Launch27

Checks a gift card discount in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `giftcard/discount`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Check Gift Card Discount](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Sender email used to validate the gift card discount code. |
| `code` | body | `string` | yes | Gift card discount code to validate. |
