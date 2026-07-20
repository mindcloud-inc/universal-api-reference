# Get blacklisted contacts for service with Routee

Retrieves blacklisted contacts for service from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/my/blacklist/:service`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get blacklisted contacts for service](https://docs.routee.net/reference/get-blacklisted-contacts-for-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | path | `string` | yes | The service (Sms, Voice, Viber, TwoStep) to get the blacklisted contacts for. |
