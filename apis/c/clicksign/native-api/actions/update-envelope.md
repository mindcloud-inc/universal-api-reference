# Update Envelope with Clicksign

Updates an existing envelope in Clicksign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/envelopes/:envelope_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Update Envelope](https://developers.clicksign.com/reference/api-editar-envelope)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_close` | body | `boolean` | no | Whether the envelope closes automatically. |
| `block_after_refusal` | body | `boolean` | no | Whether the envelope blocks after refusal. |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `data.attributes` | body | `object` | no | Envelope attributes. |
| `data.attributes.locale` | body | `string` | no | The envelope locale. |
| `data.attributes.name` | body | `string` | no | The envelope name. |
| `data.attributes.status` | body | `string` | yes | The envelope status. |
| `data.id` | body | `string` | yes | The UUID of the envelope in the JSON:API body. |
| `deadline_at` | body | `date` | no | The signing deadline timestamp. |
| `default_message` | body | `string` | no | Default notification message. |
| `default_subject` | body | `string` | no | Default notification subject. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `remind_interval` | body | `number` | no | Reminder interval in days. |
