# Send Transactional Email with GMass

Sends a transactional email through GMass.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactional`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Send Transactional Email](https://api.gmass.co/docs#tag/Transactional/operation/Transactional_IndexAsync)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `to` | body | `string` | yes |
| `subject` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromEmail` | body | `string` | yes |
| `fromName` | body | `string` | no |
| `cc` | body | `string` | no |
| `bcc` | body | `string` | no |
| `messageRaw` | body | `string` | no |
| `settings` | body | `object` | no |
| `settings.openTrack` | body | `boolean` | no |
| `settings.clickTrack` | body | `boolean` | no |
| `settings.messageType` | body | `string` | no |
