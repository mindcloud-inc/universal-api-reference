# Track Page View with LogSnag

## Endpoint

- **Method:** `POST`
- **Path:** `/page`
- **Base URL:** `https://api.logsnag.com/v1`
- **Official documentation:** [Track Page View](https://docs.logsnag.com/sdks/node)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name in LogSnag. |
| `user_id` | body | `string` | yes | User identifier for the page event. |
| `payload` | body | `object` | yes | Page payload object. Includes path and optional metadata. |
