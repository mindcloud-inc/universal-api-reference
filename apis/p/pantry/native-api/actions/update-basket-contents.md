# Update Basket Contents with Pantry

Updates basket contents in Pantry.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pantry/:pantryId/basket/:basketName`
- **Base URL:** `https://getpantry.cloud/apiv1`
- **Official documentation:** [Update Basket Contents](https://documenter.getpostman.com/view/3281832/SzmZeMLC)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basketName` | path | `string` | yes | Name of the basket to update. |
| `contents` | body | `object` | yes | JSON object to deep-merge into the existing basket. |
