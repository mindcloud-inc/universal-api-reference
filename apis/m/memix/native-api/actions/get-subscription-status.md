# Get Subscription Status with Memix

Retrieves current subscription status from Memix.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/subscriptions`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `installation_id` | query | `string` | yes | Installation identifier that Memix expects in the x-installation-id header. |
