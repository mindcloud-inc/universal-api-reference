# Remove URLs From Group with WebChange Detector

Removes URLs from a group in WebChange Detector.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/groups/:id/remove-urls`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Remove URLs From Group](https://api.webchangedetector.com/docs#group-POSTapi-v2-groups--id--remove-urls)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `urls[]` | body | `array<string>` | yes |
