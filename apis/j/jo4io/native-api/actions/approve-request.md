# Approve Transfer Request with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/transfer-request/:slug/approve`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Approve Transfer Request](https://jo4-api.jo4.io/swagger-ui/index.html#/url-transfer-request-controller/approveRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug` | path | `string` | yes |
| `transferType` | body | `string` | yes |
