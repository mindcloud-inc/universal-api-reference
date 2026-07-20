# Initiate Payment (Form Data) with aamarPay

Creates a payment request in aamarPay using form data.

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://sandbox.aamarpay.com`
- **Official documentation:** [Initiate Payment (Form Data)](https://aamarpay.readme.io/reference/initiate-payment-form-data)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tran_id` | body | `string` | yes | Unique merchant transaction id for the checkout session. |
| `success_url` | body | `string` | yes | Redirect URL after a successful payment. |
| `fail_url` | body | `string` | yes | Redirect URL after a failed payment. |
| `cancel_url` | body | `string` | yes | Redirect URL after a canceled payment. |
| `amount` | body | `string` | yes | Payment amount as a decimal string. |
| `currency` | body | `string` | yes | Transaction currency, for example BDT. |
| `desc` | body | `string` | yes | Merchant-facing description for the transaction. |
| `cus_name` | body | `string` | yes | Customer full name. |
| `cus_email` | body | `string` | yes | Customer email address. |
| `cus_add1` | body | `string` | yes | Customer primary street address. |
| `cus_city` | body | `string` | yes | Customer city. |
| `cus_country` | body | `string` | yes | Customer country. |
| `cus_phone` | body | `string` | yes | Customer phone number. |
