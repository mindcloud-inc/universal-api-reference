# Get Order Fulfillments with Rithum for Brands

Retrieve all fulfillments for a specified order.

## Endpoint

- **Method:** `GET`
- **Path:** `Orders(:orderID)/Fulfillments`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Get Order Fulfillments](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=981a17a187001e10712797d83cbb3550)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderID` | path | `string` | yes | The Rithum-generated unique identifier for the order you want to see fulfillments for. |
