# Create Subscriber Invite Token with SignalWire

Creates a new subscriber invite token in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/subscriber/invites`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create Subscriber Invite Token](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-subscriber-invite-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_id` | body | `string` | yes | Unique ID of a Subscriber Address |
| `expires_at` | body | `number` | no | A unixtime (the number of seconds since 1970-01-01 00:00:00) at which the token should no longer be valid. Defaults to 'two hours from now' |
