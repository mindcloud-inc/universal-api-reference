# Get Referrals Status with Memix

Retrieves current referral status from Memix.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/referrals-status`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `installation_id` | query | `string` | yes | Installation identifier that Memix expects in the x-installation-id header. |
