# List Fulfillments with Rithum for Brands

Retrieve existing Fulfillments.

## Endpoint

- **Method:** `GET`
- **Path:** `Fulfillments(:fullfillmentID)`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [List Fulfillments](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=13fcdf491bd5d1d42d9eea40604bcb65)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fullfillmentID` | path | `string` | no | (optional) A Rithum generated unique identifier for a specific Fulfillment. |
| `$filter` | query | `string` | no | (optional) Use a custom filter. (*oData*). **Examples**: - OrderID eq 20008076 - CreatedDateUtc ge 2016-03-02 and CreatedDateUtc lt 2016-03-03 |
| `$expand` | query | `list<string>` | no | (optional) Expand a specific sublist (i.e. Items on this Fulfillment.) |
