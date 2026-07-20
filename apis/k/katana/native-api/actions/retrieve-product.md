# Retrieve Product with Katana

Retrieves a product by ID from Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Retrieve Product](https://developer.katanamrp.com/reference/getproduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Product id |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
