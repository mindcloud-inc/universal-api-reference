# Calculate Cover Dimensions with Lulu

Calculates cover dimensions in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/cover-dimensions/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Calculate Cover Dimensions](https://api.lulu.com/docs/#tag/Cover-Dimensions/operation/Cover-Dimensions_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interior_page_count` | body | `number` | yes | Interior page count for Lulu cover dimensions. |
| `pod_package_id` | body | `string` | yes | Lulu pod package ID for cover dimensions. |
| `unit` | body | `string` | no | Output unit for Lulu cover dimensions. |
