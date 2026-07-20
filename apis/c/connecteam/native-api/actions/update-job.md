# Update Job with Connecteam

Update a single job by its unique identifier. Currently, updating job with nested sub-jobs is not supported.

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/v1/jobs/:jobId`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Update Job](https://developer.connecteam.com/reference/update_job_jobs_v1_jobs__jobId__put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobId` | path | `string` | yes |
| `title` | body | `string` | yes |
| `code` | body | `string` | no |
| `description` | body | `string` | no |
| `gps` | body | `object` | no |
| `gps.address` | body | `string` | no |
| `gps.longitude` | body | `number` | no |
| `gps.latitude` | body | `number` | no |
| `assign` | body | `object` | no |
| `assign.type` | body | `string` | no |
| `assign.userIds[]` | body | `array<number>` | no |
| `assign.groupIds[]` | body | `array<number>` | no |
| `customFields[]` | body | `array<object>` | no |
| `customFields[].customFieldId` | body | `number` | no |
| `customFields[].value` | body | `string` | no |
| `parentId` | body | `string` | no |
| `useParentData` | body | `boolean` | no |
