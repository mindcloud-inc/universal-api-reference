# Analyze Bulk Messages - Campaigns with Routee

Analyzes bulk message campaigns in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/analyze/campaign`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Analyze Bulk Messages - Campaigns](https://docs.routee.net/reference/analyze-bulk-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<string>` | no | The contact ids that the message will be sent to. At least one of "contacts", "groups" or "to" is required. |
| `groups[]` | body | `array<string>` | no | The groups of contacts in the account selected as recipients. |
| `to[]` | body | `array<string>` | no | The phone numbers the message is about to be sent to. Format with a '+' and country code e.g., +306948530920 (E.164 format). |
| `from` | body | `string` | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | body | `string` | yes | The message you want to send. |
