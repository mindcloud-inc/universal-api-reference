# Update Item Attribute with BoxHero

Updates an existing item attribute in BoxHero.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/item-attrs/:attr_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Update Item Attribute](https://rest.boxhero-app.com/docs/api#/item-attrs/BarcodeAttrsController_updateAttr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attr_id` | path | `number` | yes | Unique identifier for the item attribute |
| `name` | body | `string` | yes | Name of the item attribute |
