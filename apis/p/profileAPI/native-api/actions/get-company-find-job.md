# Get Company Find Job with profileAPI

Retrieves a company search job from profileAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/find/jobs/:jobId`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Get Company Find Job](https://documentation.profileapi.com/api-reference/get-company-find-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Company find job identifier from a create/list/latest job response. |
