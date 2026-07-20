# Update Group with WebChange Detector

Updates an existing group in WebChange Detector.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/groups/:id`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Update Group](https://api.webchangedetector.com/docs#group-PUTapi-v2-groups--id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `enabled` | body | `boolean` | no |
| `id` | path | `string` | yes |
| `monitoring` | body | `boolean` | no |
| `name` | body | `string` | no |
