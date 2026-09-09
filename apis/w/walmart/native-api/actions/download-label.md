# Download Label with Walmart

Retrieve the label for a carrier & tracking number combination. Returns PDF or PNG formatted label.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/shipping/labels/carriers/:carrierShortName/trackings/:trackingNo`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Download Label](https://developer.walmart.com/us-marketplace/reference/getlabelbytrackingandcarrier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrierShortName` | path | `string` | yes | carrierShortName |
| `trackingNo` | path | `string` | yes | The tracking number of the label to download. |
| `format` | query | `list<string>` | no | Defaults to PDF if not set. |
