# Create Stock Adjustment with Sharetribe

Creates a new stock adjustment in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `stock_adjustments/create`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Create Stock Adjustment](https://www.sharetribe.com/api-reference/integration.html#create-stock-adjustment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingId` | body | `string` | yes | The ID of the listing. |
| `quantity` | body | `number` | yes | Quantity of the stock adjustment. Positive increases stock and negative decreases stock. |
