# Set Endpoint Data Quota with EMnify

Sets a new data quota for an endpoint in EMnify.

## Endpoint

- **Method:** `POST`
- **Path:** `/endpoint/:endpoint_id/quota/data`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Set Endpoint Data Quota](https://docs.emnify.com/developers/api/endpoint/endpoint-quota-data-by-endpoint-id-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to configure. |
| `status.id` | body | `number` | yes | Quota status ID. |
| `volume` | body | `number` | yes | Remaining quota volume in MB. |
| `expiry_date` | body | `string` | yes | Quota expiry timestamp. |
| `action_on_exhaustion.id` | body | `number` | yes | Action ID to execute when the quota is exhausted. |
| `auto_refill` | body | `number` | no | Whether the quota should auto-refill daily. |
| `threshold_percentage` | body | `number` | no | Remaining quota percentage threshold for events. |
| `last_volume_added` | body | `number` | no | Last added quota volume. |
| `last_status_change_date` | body | `string` | no | Quota status change timestamp. |
| `threshold_volume` | body | `number` | no | Remaining quota volume threshold for events. |
