# Unblock MSISDN with Channels

Unblocks a phone number in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/dnclist/unblock`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Unblock MSISDN](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdns[]` | body | `array<string>` | yes | Array of phone numbers to unblock. Send multiple values as a array. |
