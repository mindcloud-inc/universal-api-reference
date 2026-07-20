# Send Bulk SMS With Source with DIDWW SMS OUT

Creates bulk outbound SMS messages in DIDWW SMS OUT with a source DID.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk_outbound_messages`
- **Base URL:** `https://us.sms-out.didww.com`
- **Official documentation:** [Send Bulk SMS With Source](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html#outbound-sms-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinations` | body | `string` | yes | Comma-separated list of recipient numbers in E.164 format. |
| `source` | body | `string` | yes | Sender DID in E.164 format. |
| `content` | body | `string` | yes | SMS body text. |
