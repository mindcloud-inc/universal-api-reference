# Get Outlet with Lightspeed Retail POS (X-Series)

Retrieves an outlet from Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/outlets/:outlet_id`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Get Outlet](https://x-series-api.lightspeedhq.com/reference/getoutletbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outlet_id` | path | `string` | yes | The Lightspeed outlet ID to retrieve. |
