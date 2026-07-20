# Create Link with OPN

Creates a new link in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/links`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Create Link](https://docs.omise.co/links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | The amount to collect, in the smallest currency unit. |
| `currency` | body | `string` | yes | The three-letter currency code. |
| `description` | body | `string` | yes | The payment link description. |
| `multiple` | body | `boolean` | no | Whether the payment link can be used multiple times. |
| `title` | body | `string` | yes | The payment link title. |
