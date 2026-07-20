# Update a Schedule with Mihu AI

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/schedules/:uuid`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Update a Schedule](https://developers.mihu.ai/api-reference/schedules/update-a-schedule)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `availability_type_uuid` | body | `string` | no |
| `color` | body | `string` | no |
| `name` | body | `string` | no |
| `uuid` | path | `string` | yes |
