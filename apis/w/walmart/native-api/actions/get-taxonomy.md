# Get Taxonomy with Walmart

Retrieve items taxonomy information.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/items/taxonomy`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Taxonomy](https://developer.walmart.com/us-marketplace/reference/gettaxonomyresponse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `list<string>` | no | The type of feed defines the nature of the request. Select an option from the drop-down list based on the type of taxonomy details you need to retrieve.  Examples: - `MP_WFS_ITEM` - indicates WFS Item - `MP_ITEM` - Indicates Seller Fulfilled Item |
| `version` | query | `list<list>` | no | The status of an item in the overall lifecycle. |
