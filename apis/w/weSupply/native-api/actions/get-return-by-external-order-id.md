# Get Return By External Order ID with WeSupply

Retrieves a return from WeSupply by external order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/returns/grabById`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Get Return By External Order ID](https://documenter.getpostman.com/view/11859344/T17AiAYq#af252121-fad4-481f-ab32-28d9318190e3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderExternalOrderID` | query | `string` | no | The external order ID associated with the return. |
