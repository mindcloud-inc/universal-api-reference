# List Floating IPs with Pilvio

## Endpoint

- **Method:** `GET`
- **Path:** `/network/ip_addresses`
- **Base URL:** `https://api.pilvio.com/v1`
- **Official documentation:** [List Floating IPs](https://api.pilvio.com/#list-floating-ips)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_account_id` | query | `string` | yes | Billing account ID used to filter floating IPs. |
