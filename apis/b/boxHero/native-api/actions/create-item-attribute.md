# Create Item Attribute with BoxHero

Creates a new item attribute in BoxHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/item-attrs`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Create Item Attribute](https://rest.boxhero-app.com/docs/api#/item-attrs/BarcodeAttrsController_createAttr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the item attribute |
| `rank` | body | `number` | yes | Rank used to sort attributes |
| `type` | body | `string` | yes | Type of value assigned to the item attribute |
