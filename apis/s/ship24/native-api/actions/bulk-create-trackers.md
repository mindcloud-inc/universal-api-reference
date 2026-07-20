# Bulk Create Trackers with Ship24

Creates multiple new trackers in Ship24.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/trackers/bulk`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Bulk Create Trackers](https://docs.ship24.com/tracking-api-reference/#/operations/bulk-create-trackers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `trackers[]` | body | `array<object>` | yes |
