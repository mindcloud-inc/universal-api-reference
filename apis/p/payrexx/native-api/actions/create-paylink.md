# Create Paylink with Payrexx

Creates a paylink in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Invoice/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Create Paylink](https://developers.payrexx.com/reference/create-a-paylink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Page title shown on the payment page. |
| `description` | body | `string` | yes | Description shown on the payment page. |
| `referenceId` | body | `string` | yes | Internal reference id used by your system. |
| `purpose` | body | `string` | yes | Purpose of the payment. |
| `amount` | body | `number` | yes | Amount in cents. |
| `currency` | body | `string` | yes | Currency code for the payment. |
