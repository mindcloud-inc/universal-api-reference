# Update Business with Hyperise

Updates an existing business in Hyperise.

## Endpoint

- **Method:** `PUT`
- **Path:** `/businesses/:businessId`
- **Base URL:** `https://app.hyperise.io/api/v1/regular`
- **Official documentation:** [Update Business](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_name` | body | `string` | no | Updated business name. |
| `businessId` | path | `string` | yes | The Hyperise business record ID. |
| `email` | body | `string` | no | Updated business contact email. |
| `website` | body | `string` | no | Updated business website. |
