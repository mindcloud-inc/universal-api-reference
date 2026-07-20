# Create Meeting with Webex

Creates a new meeting in Webex.

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Create Meeting](https://developer.webex.com/meeting/docs/api/v1/meetings/create-a-meeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Meeting title. |
| `start` | body | `date` | yes | Meeting start time in ISO-8601 format. |
| `end` | body | `date` | yes | Meeting end time in ISO-8601 format. |
