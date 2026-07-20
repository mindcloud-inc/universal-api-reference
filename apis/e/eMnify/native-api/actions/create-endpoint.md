# Create Endpoint with EMnify

Creates a new endpoint in EMnify.

## Endpoint

- **Method:** `POST`
- **Path:** `/endpoint`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Create Endpoint](https://docs.emnify.com/developers/api/endpoint/create-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `service_profile.id` | body | `number` | yes | Service profile ID that determines network access settings. |
| `tariff_profile.id` | body | `number` | yes | Tariff profile ID that determines pricing and data limits. |
| `status.id` | body | `number` | yes | Initial endpoint status ID. |
| `name` | body | `string` | no | Display name for the endpoint. |
| `tags` | body | `string` | no | Comma-separated endpoint tags. |
| `imei` | body | `string` | no | IMEI with software version number. |
| `imei_lock` | body | `boolean` | no | Only allow connections from the specified IMEI. |
| `sim.id` | body | `number` | no | SIM ID to assign to the endpoint. |
| `sim.activate` | body | `boolean` | no | Activate the assigned SIM during endpoint creation. |
| `ip_address` | body | `string` | no | Private IP address to assign. |
| `ip_address_space.id` | body | `number` | no | IP address space ID required when an IP address is provided. |
| `organisation.id` | body | `number` | no | Organization ID for reseller-created endpoints. |
