# Send SMS With Source with DIDWW SMS OUT

Creates an outbound SMS in DIDWW SMS OUT with a source DID.

## Endpoint

- **Method:** `POST`
- **Path:** `/outbound_messages`
- **Base URL:** `https://us.sms-out.didww.com`
- **Official documentation:** [Send SMS With Source](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html#outbound-sms-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | yes | Recipient number in E.164 format. |
| `source` | body | `string` | yes | Sender DID in E.164 format. |
| `content` | body | `string` | yes | SMS body text. |
