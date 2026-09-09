# Get Taxonomy by Spec with Walmart

Retrieve a list of all Categories and Sub-categories that are available on Walmart.com for the Item spec version you specify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/utilities/taxonomy`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Taxonomy by Spec](https://developer.walmart.com/us-marketplace/reference/gettaxonomyresponse-1)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `list<string>` | no | The type of feed specifies the nature of the update. Select an option from the drop-down list based on the type of update you need to perform. Example: MP_WFS_ITEM indicates the new WFS Item set up. |
| `version` | query | `list<list>` | no | Specifies the version for the `feedType` |
