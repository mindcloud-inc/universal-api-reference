# Create Template with Mailcoach

Creates a new template in Mailcoach.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Create Template](https://www.mailcoach.app/api-documentation/endpoints/templates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | The template HTML content. |
| `name` | body | `string` | yes | The name of the template. |
| `structured_html` | body | `object` | no | The structured HTML payload for the template. |
