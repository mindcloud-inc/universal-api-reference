# Create Envelope with Clicksign

Creates an envelope in Clicksign.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelopes`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Create Envelope](https://developers.clicksign.com/reference/api-criar-envelope)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_close` | body | `boolean` | no | Whether the envelope closes automatically. |
| `block_after_refusal` | body | `boolean` | no | Whether the envelope blocks after refusal. |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `data.attributes` | body | `object` | no | Envelope attributes. |
| `data.attributes.locale` | body | `string` | no | The envelope locale. |
| `data.attributes.name` | body | `string` | yes | The envelope name. |
| `deadline_at` | body | `date` | no | The signing deadline timestamp. |
| `default_message` | body | `string` | no | Default notification message. |
| `default_subject` | body | `string` | no | Default notification subject. |
| `remind_interval` | body | `number` | no | Reminder interval in days. |
