# Get Public Basket ID with Pantry

Retrieves a public basket ID from Pantry.

## Endpoint

- **Method:** `GET`
- **Path:** `/pantry/:pantryId/basket/:basketName/public`
- **Base URL:** `https://getpantry.cloud/apiv1`
- **Official documentation:** [Get Public Basket ID](https://documenter.getpostman.com/view/3281832/SzmZeMLC)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basketName` | path | `string` | yes | Name of the basket to expose publicly. |
