# Get User with Lightspeed Retail POS (X-Series)

Retrieves a user from Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/users/:user_id`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Get User](https://x-series-api.lightspeedhq.com/reference/getuserbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | The Lightspeed user ID to retrieve. |
