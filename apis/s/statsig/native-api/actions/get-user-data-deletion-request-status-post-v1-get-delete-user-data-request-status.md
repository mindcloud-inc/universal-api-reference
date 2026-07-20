# Get User Data Deletion Request Status with Statsig

Retrieves a user data deletion request status from Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_delete_user_data_request_status`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get User Data Deletion Request Status](https://docs.statsig.com/compliance/user_data_deletion_requests/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | body | `string` | yes | Deletion request ID returned by Create User Data Deletion Request. |
