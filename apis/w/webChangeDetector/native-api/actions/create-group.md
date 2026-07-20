# Create Group with WebChange Detector

Creates a new group in WebChange Detector.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/groups`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Create Group](https://api.webchangedetector.com/docs#group-POSTapi-v2-groups)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `enabled` | body | `boolean` | no |
| `monitoring` | body | `boolean` | no |
| `name` | body | `string` | yes |
