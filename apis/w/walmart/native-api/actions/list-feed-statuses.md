# List Feed Statuses with Walmart

Returns the feed statuses for all the specified Feed IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Feed Statuses](https://developer.walmart.com/us-marketplace/reference/getallfeedstatuses#:~:text=Utilities-,All%20feed%20statuses,-GET)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedId` | query | `string` | no | Unique ID returned by a bulk request. Used to track a Feed file. |
| `feedType` | query | `list<string>` | no | Define a type of feed to retrieve. #### Market Availability Feed types are specific to each market. These examples are not an exhaustive list.  - *__Global__*: `MP_MAINTENANCE`, `MP_ITEM_MATCH`, `LAGTIME` - *__US, CA, MX__*: `MP_INVENTORY`, `SKU_TEMPLATE_MAP` - *__CA, MX, CL__*: `MP_ITEM_INTL` - *__US Only__*: `MP_ITEM`, `MP_WFS_ITEM`, `WALMART_FUNDED_INCENTIVES_ENROLLMENT`, `INCENTIVE_ENROLLMENT`, `PRICE_AND_PROMOTION`, `OMNI_WFS`, `RETIRE_ITEM`, `SHIPPING_OVERRIDES`, `FITMENT_ACES`, `FITMENT_PIES`, `SPLIT_AND_MERGE` - *__CA, MX__*: `OMNI_WFSSETUP`, `OMNI_WFSCONVERT` |
| `feedStatus` | query | `list<string>` | no | Status of the feed.  Allowed: - RECEIVED - INPROGRESS - PROCESSED - ERROR |
