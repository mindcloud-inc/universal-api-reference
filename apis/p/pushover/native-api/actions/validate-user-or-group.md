# Validate User or Group with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/users/validate.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Validate User or Group](https://pushover.net/api#validate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | yes | User key or group key to validate. |
| `device` | query | `string` | no | Optional device name to validate. |
