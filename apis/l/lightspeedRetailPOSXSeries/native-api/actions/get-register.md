# Get Register with Lightspeed Retail POS (X-Series)

Retrieves a register from Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/registers/:register_id`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Get Register](https://x-series-api.lightspeedhq.com/reference/getregisterbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `register_id` | path | `string` | yes | The register ID. |
