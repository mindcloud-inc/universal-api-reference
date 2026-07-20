# Create Orders with Revi.io Reviews

Creates orders in Revi.io Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Create Orders](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | Array of Revi order objects to create or update. |
