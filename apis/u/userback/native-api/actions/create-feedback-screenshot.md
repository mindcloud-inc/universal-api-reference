# Create Feedback Screenshot with Userback

Creates a screenshot for a Userback feedback item.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback/screenshot`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Create Feedback Screenshot](https://docs.userback.io/reference/createscreenshot)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedbackId` | body | `number` | yes | Parent feedback ID. |
| `files` | body | `file` | yes | One or more screenshot files to upload. |
