# List Leads with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [List Leads](https://docs.housecallpro.com/docs/housecall-public-api/278974bc87e32-get-leads)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `string` | no | Filters leads by a single customer ID (string) |
| `status` | query | `list` | no | Filters leads by status Accepted values: `lost`, `open`, `won`. |
| `lead_source[]` | query | `array<string>` | no | Filters leads by a single lead_source |
| `employee_ids[]` | query | `array<string>` | no | Filters leads by a list of employee IDs (string) |
| `tag_ids[]` | query | `array<string>` | no | Filters leads by a list of tags |
| `location_ids[]` | query | `array<string>` | no | IDs of locations to pull from. Ignored when X-Company-Id is set. |
