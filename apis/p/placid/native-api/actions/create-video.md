# Create Video with Placid

Creates a new video in Placid from template clips.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/videos`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Create Video](https://placid.app/docs/2.0/rest/videos#create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhook_success` | body | `string` | no |
| `passthrough` | body | `string` | no |
| `clips[]` | body | `array<object>` | no |
| `clips[].template_uuid` | body | `string` | no |
| `clips[].layers` | body | `object` | no |
| `transfer` | body | `object` | no |
| `modifications` | body | `object` | no |
