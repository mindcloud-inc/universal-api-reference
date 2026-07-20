# Get Tracking with Ship&Co

## Endpoint

- **Method:** `GET`
- **Path:** `/tracking/:carrier/:trackingNumber`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Get Tracking](https://developer.shipandco.com/en/#tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrier` | path | `string` | yes | Carrier code such as dhl, ups, fedex, japanpost, sagawa, yamato, or yuupack. |
| `trackingNumber` | path | `string` | yes | Carrier tracking number. |
