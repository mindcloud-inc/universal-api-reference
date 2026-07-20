# Create Jobs with Connecteam

Create individual or multiple jobs under a specified scheduler

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/v1/jobs`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Create Jobs](https://developer.connecteam.com/reference/create_jobs_jobs_v1_jobs_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobs[]` | body | `array<object>` | no |
| `jobs[].instanceIds[]` | body | `array<number>` | yes |
| `jobs[].title` | body | `string` | yes |
| `jobs[].code` | body | `string` | no |
| `jobs[].description` | body | `string` | no |
| `jobs[].gps` | body | `object` | no |
| `jobs[].gps.address` | body | `string` | no |
| `jobs[].gps.longitude` | body | `number` | no |
| `jobs[].gps.latitude` | body | `number` | no |
| `jobs[].assign` | body | `object` | no |
| `jobs[].assign.type` | body | `string` | no |
| `jobs[].assign.userIds[]` | body | `array<number>` | no |
| `jobs[].assign.groupIds[]` | body | `array<number>` | no |
| `jobs[].customFields[]` | body | `array<object>` | no |
| `jobs[].customFields[].customFieldId` | body | `number` | no |
| `jobs[].customFields[].value` | body | `string` | no |
| `jobs[].color` | body | `string` | no |
| `jobs[].subJobs[]` | body | `array<object>` | no |
| `jobs[].subJobs[].title` | body | `string` | yes |
| `jobs[].subJobs[].code` | body | `string` | no |
| `jobs[].subJobs[].description` | body | `string` | no |
| `jobs[].subJobs[].gps` | body | `object` | no |
| `jobs[].subJobs[].gps.address` | body | `string` | no |
| `jobs[].subJobs[].gps.longitude` | body | `number` | no |
| `jobs[].subJobs[].gps.latitude` | body | `number` | no |
| `jobs[].subJobs[].assign` | body | `object` | no |
| `jobs[].subJobs[].assign.type` | body | `string` | no |
| `jobs[].subJobs[].assign.userIds[]` | body | `array<number>` | no |
| `jobs[].subJobs[].assign.groupIds[]` | body | `array<number>` | no |
| `jobs[].subJobs[].customFields[]` | body | `array<object>` | no |
| `jobs[].subJobs[].customFields[].customFieldId` | body | `number` | no |
| `jobs[].subJobs[].customFields[].value` | body | `string` | no |
| `jobs[].subJobs[].useParentData` | body | `boolean` | no |
