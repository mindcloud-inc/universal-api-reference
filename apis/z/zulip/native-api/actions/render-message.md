# Render Message with Zulip

Renders Zulip message content into HTML.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/render`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Render Message](https://zulip.com/api/render-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The Markdown message content to render. |
