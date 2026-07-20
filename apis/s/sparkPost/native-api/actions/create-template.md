# Create Template with SparkPost

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Create Template](https://developers.sparkpost.com/api/templates/#templates-post-create-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content.from.email` | body | `string` | yes | Sender email address for the template draft. |
| `content.from.name` | body | `string` | no | Sender display name for the template draft. |
| `content.html` | body | `string` | no | HTML body for the template. |
| `content.subject` | body | `string` | no | Default message subject. |
| `content.text` | body | `string` | no | Plain-text content for the template draft. |
| `id` | body | `string` | yes | Unique template identifier. |
| `name` | body | `string` | no | Human-readable template name. |
