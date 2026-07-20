# Block MSISDN with Channels

Blocks a phone number in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/dnclist/block`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Block MSISDN](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdns[]` | body | `array<string>` | yes | Array of phone numbers to block. Send multiple values as a array. |
