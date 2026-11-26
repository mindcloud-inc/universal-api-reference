# Get Seller Events with eBay

Use this call to retrieve a list of the items on which a seller event has occurred. A seller event includes actions such as a revision to the item (e.g., a description change), a price change (through a bid), or the ending of an item's listing.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.ebay.com/ws/api.dll`
- **API:** REST eBay XML
- **Official documentation:** [Get Seller Events](https://developer.ebay.com/devzone/xml/docs/reference/ebay/GetSellerEvents.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modTimeTo` | body | `date` | no | — |
| `modTimeFrom` | body | `date` | no | — |
| `startTimeFrom` | body | `date` | no | — |
| `startTimeTo` | body | `date` | no | — |
| `endTimeFrom` | body | `date` | no | Describes the earliest (oldest) date to use in a time range filter based on item end time. Must be specified if EndTimeTo is specified. |
| `endTimeTo` | body | `date` | no | Describes the latest (most recent) date to use in a time range filter based on item end time.  If you specify the corresponding From filter, but you do not include EndTimeTo, then EndTimeTo is set to the time you make the call. |
| `newItemFilter` | body | `boolean` | no | — |
| `includeWatchCount` | body | `boolean` | no | — |
