# View surcharge recommendation with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/surcharge`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [View surcharge recommendation](https://docs.nexiopay.com/reference/viewsurchargerecommendation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Transaction data object documented by Nexio. |
| `card` | body | `object` | no | Card information object documented by Nexio. |
| `tokenex` | body | `object` | no | TokenEx payment token object documented by Nexio. |
