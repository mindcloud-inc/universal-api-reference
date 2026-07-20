# Set Inbound Call Forwarding with Channels

Updates inbound call forwarding for a phone number in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/inbound/configuration/numbers/{msisdnId}/forward`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Set Inbound Call Forwarding](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdnId` | path | `number` | yes | Phone number ID whose forwarding configuration should be updated. |
| `phoneNumber` | body | `string` | yes | Phone number where incoming calls should be forwarded. |
