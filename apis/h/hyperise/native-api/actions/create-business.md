# Create Business with Hyperise

Creates a new business in Hyperise.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses`
- **Base URL:** `https://app.hyperise.io/api/v1/regular`
- **Official documentation:** [Create Business](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_name` | body | `string` | yes | The business name. |
| `email` | body | `string` | yes | The business contact email. |
| `website` | body | `string` | yes | The business website. |
