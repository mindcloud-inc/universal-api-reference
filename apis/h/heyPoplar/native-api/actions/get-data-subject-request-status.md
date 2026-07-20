# Get Data Subject Request Status with HeyPoplar

Retrieves a data subject request status from HeyPoplar.

## Endpoint

- **Method:** `GET`
- **Path:** `/dsr/request/:subject_request_id`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [Get Data Subject Request Status](https://docs.heypoplar.com/api/endpoints/data-subject-requests#fetch-data-subject-request-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_request_id` | path | `string` | yes | The subject_request_id returned by the create request. |
