# List Site Availability with Emporix Commerce Engine

Retrieves site availability from Emporix Commerce Engine.

## Endpoint

- **Method:** `GET`
- **Path:** `/availability/{tenantId}/availability/site/:site`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [List Site Availability](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/availability/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | path | `string` | yes | The Emporix site code to retrieve availability for. |
