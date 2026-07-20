# Update Template with Mailcoach

Updates an existing template in Mailcoach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/:uuid`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Update Template](https://www.mailcoach.app/api-documentation/endpoints/templates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | The template HTML content. |
| `name` | body | `string` | yes | The name of the template. |
| `structured_html` | body | `object` | no | The structured HTML payload for the template. |
| `uuid` | path | `string` | yes | The UUID of the template to update. |
