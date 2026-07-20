# Create Feedback Object with Nicereply

Creates a feedback object in Nicereply.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback-objects`
- **Base URL:** `https://api.nicereply.com`
- **Official documentation:** [Create Feedback Object](https://cdn.nicereply.com/s/api/latest/reference/feedback-objects/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Unique email address for the feedback object. |
| `full_name` | body | `string` | yes | Display name for the feedback object. |
| `username` | body | `string` | yes | Unique username for the feedback object. |
