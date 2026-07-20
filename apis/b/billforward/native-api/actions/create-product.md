# Create Product with Billforward

Creates a new product in Billforward.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://app-sandbox.billforward.net/v1`
- **Official documentation:** [Create Product](https://app.billforward.net/#/api/method/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Product name. |
| `description` | body | `string` | yes | Product description. |
| `duration` | body | `number` | yes | Product duration value. |
| `durationPeriod` | body | `string` | yes | Duration period unit. |
| `productType` | body | `string` | yes | Billforward product type. |
| `trial` | body | `number` | yes | Trial duration value. |
| `trialPeriod` | body | `string` | yes | Trial period unit. |
