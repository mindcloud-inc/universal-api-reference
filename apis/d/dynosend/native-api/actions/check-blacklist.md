# Check Blacklist with Dynosend

Checks whether a contact is blacklisted in Dynosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/blacklist`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Check Blacklist](https://developers.dynosend.com/#checkacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to check against the blacklist. |
