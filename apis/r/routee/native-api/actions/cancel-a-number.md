# Cancel a Number with Routee

Cancels an existing number in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/numbers/my/:msisdn`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Cancel a Number](https://docs.routee.net/reference/cancel-a-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | path | `string` | yes | The phone number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |
