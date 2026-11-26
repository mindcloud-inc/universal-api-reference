# Get Orders with eBay

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.ebay.com/ws/api.dll`
- **API:** REST eBay XML
- **Official documentation:** [Get Orders](https://developer.ebay.com/devzone/xml/docs/reference/ebay/getorders.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CreateTimeFrom` | body | `date` | yes | Start of the order creation time window. eBay requires the CreateTimeFrom/CreateTimeTo range to be no more than 90 days. |
| `CreateTimeTo` | body | `date` | no | End of the order creation time window. eBay recommends sellers set this to current time minus 2 minutes. |
