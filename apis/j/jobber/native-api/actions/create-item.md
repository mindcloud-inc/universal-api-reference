# Create Item with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Create Item](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.name` | body | `string` | yes | Name of the product or service item. |
| `variables.input.defaultUnitCost` | body | `number` | yes | Default price for the service or product. |
| `variables.input.category` | body | `list` | no | Whether this item will be a product or a service. Accepted values: `PRODUCT`, `SERVICE`. |
| `variables.input.description` | body | `string` | no | Description for the service or product. |
| `variables.input.taxable` | body | `boolean` | no | Whether the product or service will be taxable. |
| `variables.input.internalUnitCost` | body | `number` | no | Default unit cost for the product or service. |
| `variables.input.markup` | body | `number` | no | Default markup for the product or service. |
| `variables.input.durationMinutes` | body | `number` | no | Duration to complete the service in minutes. |
| `variables.input.onlineBookingsEnabled` | body | `boolean` | no | Whether the product or service is available as a bookable service. |
