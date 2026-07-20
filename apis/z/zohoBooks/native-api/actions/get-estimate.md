# Get Estimate with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates/:estimate_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Get Estimate](https://www.zoho.com/books/api/v3/estimates/#get-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate_id` | path | `list` | yes | — |
| `organization_id` | query | `list` | yes | — |
| `print` | query | `boolean` | no | — |
| `accept` | query | `list` | no | Accepted values: `0`, `1`, `2`. |
