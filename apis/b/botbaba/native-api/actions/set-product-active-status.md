# Set Product Active Status with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/EditProductActiveStatus`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Set Product Active Status](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Product identifier. |
| `isActive` | body | `boolean` | yes | Whether the product is active. |
