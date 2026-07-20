# Update URL with WebChange Detector

Updates an existing URL in WebChange Detector.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/urls/:id`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Update URL](https://api.webchangedetector.com/docs#url-PUTapi-v2-urls--id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `url` | body | `string` | yes |
