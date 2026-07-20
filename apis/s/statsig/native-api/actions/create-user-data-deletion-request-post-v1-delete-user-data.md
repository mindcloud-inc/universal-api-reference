# Create User Data Deletion Request with Statsig

Creates a user data deletion request in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/delete_user_data`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create User Data Deletion Request](https://docs.statsig.com/compliance/user_data_deletion_requests/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unit_type` | body | `string` | yes | Unit type for deletion. Statsig currently supports user_id. |
| `ids` | body | `string` | yes | Delimited list of IDs to delete data for. |
| `delimiter` | body | `string` | no | Optional delimiter when IDs contain commas. |
| `request_id` | body | `string` | no | Optional unique request ID to track the deletion request. |
