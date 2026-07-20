# Create Products with Revi.io Reviews

Creates products in Revi.io Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Create Products](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products[]` | body | `array<object>` | yes | Array of Revi product objects to create or update. |
