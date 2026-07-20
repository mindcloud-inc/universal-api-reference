# Create shortlink with Webex Interact

Creates a new shortlink in Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/assets/v1/shortlink`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Create shortlink](https://docs.webexinteract.com/reference/shortlinks-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Shortlink title. |
| `target_url` | body | `string` | yes | Destination URL for the shortlink. |
| `tags` | body | `list<string>` | no | Optional array of tag strings. |
| `track_clicks` | body | `boolean` | no | Whether to track clicks. |
