# Get Supported Carrier Package Types with Walmart

Retrieves supported package types for a selected carrier.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/shipping/labels/carriers/:carrierShortName/package-types`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Supported Carrier Package Types](https://developer.walmart.com/us-marketplace/reference/getcarrierpackagetypes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrierShortName` | path | `string` | yes | Provide a `carrierShortName` or pass `ALL` to fetch all package types of supported carriers |
