# Retrieve Order Stats with Hyperzod

Retrieves order statistics from Hyperzod by delivery date.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/v1/order/stats`
- **Base URL:** `https://api.hyperzod.app`
- **Official documentation:** [Retrieve Order Stats](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-C0-Qx9TbWU7QiuU1PDxCN)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `delivery_timestamp_from` | body | `string` | yes |
| `delivery_timestamp_to` | body | `string` | yes |
