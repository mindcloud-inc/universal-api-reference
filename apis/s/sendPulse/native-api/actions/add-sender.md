# Add Sender with SendPulse

Creates a sender address in SendPulse.

## Endpoint

- **Method:** `POST`
- **Path:** `/senders`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Add Sender](https://sendpulse.com/integrations/api/bulk-email#add-sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the sender. |
| `email` | body | `string` | yes | Email address to register as a sender. |
