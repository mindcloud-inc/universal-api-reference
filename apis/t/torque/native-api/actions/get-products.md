# Get Products with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Products](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Optional product status filter: active, inactive, draft, or archived. Accepted values: `0`, `1`, `2`, `3`. |
