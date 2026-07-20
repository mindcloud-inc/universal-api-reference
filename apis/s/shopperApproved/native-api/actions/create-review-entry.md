# Create Review Entry with Shopper Approved

Creates a new review entry in Shopper Approved.

## Endpoint

- **Method:** `POST`
- **Path:** `/reviews/:siteid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [Create Review Entry](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The customer's email address. |
| `followup` | body | `date` | yes | The follow-up date in YYYY-MM-DD format. |
| `orderid` | body | `string` | yes | The unique order ID. |
| `name` | body | `string` | no | The customer's name. |
| `products` | body | `string` | no | Comma-separated product IDs to attach to the review. |
| `test` | body | `boolean` | no | Whether the review entry is a test. |
| `custom_questions` | body | `string` | no | A JSON-encoded object of custom question values. |
