# Find Customers By Segment with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/find`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Find Customers By Segment](https://docs.vouchery.io/reference/postapiv21customersfind)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_name` | body | `string` | yes | Segment category name. |
| `category_tag` | body | `string` | yes | Segment category tag. |
