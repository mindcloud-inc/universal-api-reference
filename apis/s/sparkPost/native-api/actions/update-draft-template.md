# Update Draft Template with SparkPost

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Update Draft Template](https://developers.sparkpost.com/api/templates/#templates-put-update-a-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content.html` | body | `string` | no | Updated HTML body for the draft. |
| `content.subject` | body | `string` | no | Updated message subject. |
| `id` | path | `string` | yes | Template identifier. |
| `name` | body | `string` | no | Updated template name. |
