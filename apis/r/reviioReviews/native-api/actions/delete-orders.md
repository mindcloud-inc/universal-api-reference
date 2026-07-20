# Delete Orders with Revi.io Reviews

Deletes orders from Revi.io Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Delete Orders](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | Array of orders to delete using delete=1. |
