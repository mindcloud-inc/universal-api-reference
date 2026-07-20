# Create Events with Bento Now

Tracks user activity in Bento Now.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/events`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Create Events](https://bentonow.com/docs/events_api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `events[].email` | body | `string` | yes |
| `events[].type` | body | `string` | yes |
