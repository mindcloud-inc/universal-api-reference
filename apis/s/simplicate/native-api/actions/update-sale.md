# Update Sale with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/sales/sales/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Sale](https://developer.simplicate.com/docs/api/v2/reference/update-sales-sales/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The sale id |
| `note` | body | `string` | no | A note for the sale |
| `subject` | body | `string` | no | The sale subject |
