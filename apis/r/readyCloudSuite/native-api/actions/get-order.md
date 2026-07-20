# Get Order with ReadyCloud Suite

Retrieves an order from ReadyCloud Suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Get Order](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-02-orders.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
