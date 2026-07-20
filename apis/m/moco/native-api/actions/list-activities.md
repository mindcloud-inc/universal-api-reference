# List Activities with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/activities`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Activities](https://everii-group.github.io/mocoapp-api-docs/sections/activities.html#get-activities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billable` | query | `boolean` | no |
| `billed` | query | `boolean` | no |
| `company_id` | query | `number` | no |
| `custom_properties` | query | `object` | no |
| `from` | query | `date` | no |
| `ids` | query | `string` | no |
| `project_id` | query | `number` | no |
| `task_id` | query | `number` | no |
| `term` | query | `string` | no |
| `to` | query | `date` | no |
| `updated_after` | query | `date` | no |
| `user_id` | query | `number` | no |
