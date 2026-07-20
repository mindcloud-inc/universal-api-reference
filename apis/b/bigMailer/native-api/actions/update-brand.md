# Update Brand with BigMailer

Updates an existing brand in BigMailer.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Update Brand](https://docs.bigmailer.io/reference/updatebrand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to update. |
| `name` | body | `string` | no | Name of the brand. |
| `from_name` | body | `string` | no | Default sender name for the brand. |
| `from_email` | body | `string` | no | Default sender email for the brand. |
| `bounce_danger_percent` | body | `number` | no | Bounce percentage that pauses bulk campaigns automatically. |
| `max_soft_bounces` | body | `number` | no | Maximum number of soft bounces before a contact is treated as undeliverable. |
| `url` | body | `string` | no | Website URL associated with the brand. |
| `unsubscribe_text` | body | `string` | no | Message displayed on the brand unsubscribe page. |
| `contact_limit` | body | `number` | no | Maximum number of contacts allowed in the brand. |
| `logo` | body | `string` | no | Base64 encoded brand logo image. |
| `connection_id` | body | `string` | no | ID of the sending connection used by the brand. |
