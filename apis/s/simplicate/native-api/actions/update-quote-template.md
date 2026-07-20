# Update Quote Template with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/sales/quote/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Quote Template](https://developer.simplicate.com/docs/api/v2/reference/update-sales-quote/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_reference` | body | `string` | no | The customer reference |
| `id` | path | `string` | yes | The quote template id |
| `quote_subject` | body | `string` | no | The quote subject |
