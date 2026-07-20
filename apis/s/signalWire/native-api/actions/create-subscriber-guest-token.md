# Create Subscriber Guest Token with SignalWire

Creates a new subscriber guest token in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/guests/tokens`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create Subscriber Guest Token](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-subscriber-guest-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowed_addresses[]` | body | `array<string>` | yes | List of up to 10 UUIDs representing the allowed Fabric addresses. |
| `expire_at` | body | `number` | no | A unixtime (the number of seconds since 1970-01-01 00:00:00) at which the token should no longer be valid. Defaults to 'two hours from now' |
