# Get Catalog Change Log with Rithum DSCO

Retrieves the catalog change log from Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `catalog/log`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Catalog Change Log](https://api.dsco.io/doc/v3/reference/#tag/Catalog/operation/getCatalogChangeLog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrollId` | query | `string` | no | Scroll identifier for DSCO change-log pagination. |
| `startDate` | query | `date` | no | Start date for DSCO change-log filtering. |
| `endDate` | query | `date` | no | End date for DSCO change-log filtering. |
