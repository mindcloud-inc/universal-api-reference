# Create 3rd Party Fulfillment Center Association with Walmart

Associate a third party fulfillment center with Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/settings/shipping/3plshipnodes`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Create 3rd Party Fulfillment Center Association](https://developer.walmart.com/us-marketplace/reference/associate3pfulfillmentcenter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipNode[].shipNode` | body | `string` | no | The fulfillment center (ship node) which uniquely identifies each facility and is retrieved from the `List 3PL Providers` action. |
| `shipNodeHeader` | body | `object` | no | — |
| `shipNodeHeader.version` | body | `string` | no | Example: `1.2` |
| `shipNode[]` | body | `array` | no | — |
| `shipNode[].status` | body | `list` | no | Status of fulfillment center. Allowed values: `ACTIVE`, `INACTIVE` |
