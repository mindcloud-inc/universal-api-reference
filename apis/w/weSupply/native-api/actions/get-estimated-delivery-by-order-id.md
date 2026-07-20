# Get Estimated Delivery By Order ID with WeSupply

Retrieves estimated delivery details from WeSupply by order ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/getEstimatedDeliveryByOrderId`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Get Estimated Delivery By Order ID](https://documenter.getpostman.com/view/11859344/T17AiAYq#a50a26e5-7690-42ce-90c7-f311c402ca2b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderExternalOrderID` | body | `string` | yes | The external order identifier used in WeSupply to look up the delivery estimate. |
