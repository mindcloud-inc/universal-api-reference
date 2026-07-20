# Send Email with Lettermint

Sends a single email through Lettermint.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://api.lettermint.co/v1`
- **Official documentation:** [Send Email](https://lettermint.co/docs/api-reference/sending/send#send-an-email)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `from` | body | `string` | yes |
| `subject` | body | `string` | yes |
| `to[]` | body | `array<string>` | yes |
| `html` | body | `string` | no |
| `text` | body | `string` | no |
| `tag` | body | `string` | no |
