# Create Or Replace Basket with Pantry

Creates or replaces a basket in Pantry.

## Endpoint

- **Method:** `POST`
- **Path:** `/pantry/:pantryId/basket/:basketName`
- **Base URL:** `https://getpantry.cloud/apiv1`
- **Official documentation:** [Create Or Replace Basket](https://documenter.getpostman.com/view/3281832/SzmZeMLC)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basketName` | path | `string` | yes | Name of the basket to create or replace. |
| `contents` | body | `object` | yes | JSON object to store in the basket. |
