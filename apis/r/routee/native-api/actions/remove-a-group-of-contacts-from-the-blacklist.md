# Remove a group of contacts from the blacklist with Routee

Removes a group of contacts from the blacklist in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/my/blacklist/:service/groups`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Remove a group of contacts from the blacklist](https://docs.routee.net/reference/remove-a-group-of-contacts-from-the-blacklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | path | `string` | yes | — |
| `serviceName` | path | `string` | yes | The name of the service that the blacklist refers to (Sms, TwoStep) |
