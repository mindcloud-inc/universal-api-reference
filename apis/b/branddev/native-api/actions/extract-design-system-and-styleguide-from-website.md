# Extract Design System and Styleguide from Website with Brand.dev

Retrieves website styleguide data from Brand.dev.

## Endpoint

- **Method:** `GET`
- **Path:** `/brand/styleguide`
- **Base URL:** `https://api.brand.dev/v1`
- **Official documentation:** [Extract Design System and Styleguide from Website](https://docs.context.dev/api-reference/screenshot-styleguide/extract-design-system-and-styleguide-from-website)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directUrl` | query | `string` | no | Specific URL to fetch the styleguide from directly. |
| `domain` | query | `string` | no | Domain name to extract a styleguide from. |
