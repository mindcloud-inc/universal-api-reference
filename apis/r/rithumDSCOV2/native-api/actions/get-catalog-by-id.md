# Get Catalog Object with Rithum DSCO

Retrieves a catalog item from Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `catalog`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Catalog Object](https://api.dsco.io/doc/v3/reference/#tag/Catalog/operation/getCatalogById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemKey` | query | `string` | yes | Required identifier key used to find the catalog object. |
| `value` | query | `string` | yes | Required identifier value used to find the catalog object. |
