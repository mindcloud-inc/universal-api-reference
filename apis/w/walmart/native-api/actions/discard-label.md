# Discard Label with Walmart

Mark a generated label as discarded.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/shipping/labels/carriers/:carrierShortName/trackings/:trackingNo`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Discard Label](https://developer.walmart.com/us-marketplace/reference/discardlabel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrierShortName` | path | `string` | yes | `carrierShortName` from getCarriers API |
| `trackingNo` | path | `string` | yes | — |
