# Create Data Subject Request with HeyPoplar

Creates a data subject request in HeyPoplar.

## Endpoint

- **Method:** `POST`
- **Path:** `/dsr/request`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [Create Data Subject Request](https://docs.heypoplar.com/api/endpoints/data-subject-requests#create-data-subject-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_request_id` | body | `string` | yes | Unique UUID v4 identifier for the request. |
| `subject_request_type` | body | `string` | yes | Request type. Supported values: access or erasure. |
| `submitted_time` | body | `string` | yes | ISO8601 datetime for when the request was submitted. |
| `subject_identities[]` | body | `array<object>` | yes | Array of subject identity objects with identity_type, identity_format, and identity_value. |
