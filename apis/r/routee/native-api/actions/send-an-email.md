# Send an email with Routee

Sends an email message with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/smtp/emails`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send an email](https://docs.routee.net/reference/sending-an-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email[]` | body | `array<string>` | no | a serialized array with email data |
