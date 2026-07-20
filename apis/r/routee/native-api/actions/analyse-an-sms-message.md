# Analyse an SMS message with Routee

Analyzes an SMS message in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/analyze`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Analyse an SMS message](https://docs.routee.net/reference/smsanalyze)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | body | `string` | yes | The message you want to send. |
| `to` | body | `string` | yes | The destination phone number. Format with a '+' and country code e.g., +306948530920 (E.164 format). |
