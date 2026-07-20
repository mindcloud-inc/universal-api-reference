# Create Sender with Pushpad

Creates a new sender in Pushpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/senders`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Create Sender](https://pushpad.xyz/docs/rest_api#senders_api_docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `vapid_private_key` | body | `string` | no |
| `vapid_public_key` | body | `string` | no |
