# List Group URLs with WebChange Detector

Retrieves URLs for a group from WebChange Detector.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/groups/:id/urls`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [List Group URLs](https://api.webchangedetector.com/docs#group-GETapi-v2-groups--id--urls)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `category` | body | `string` | no |
| `id` | path | `string` | yes |
| `per_page` | body | `number` | no |
| `search` | body | `string` | no |
| `type` | body | `string` | no |
| `url_ids` | body | `string` | no |
