# List Affiliate Customer Connections with GoAffPro

Retrieves affiliate customer connections from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/connections`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Affiliate Customer Connections](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return connections for this affiliate ID. |
| `customer_email` | query | `string` | no | Only return connections for this customer email address. |
