# Add URLs To Group with WebChange Detector

Adds URLs to a group in WebChange Detector.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/groups/:id/add-urls`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Add URLs To Group](https://api.webchangedetector.com/docs#group-POSTapi-v2-groups--id--add-urls)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `urls[]` | body | `array<object>` | yes |
