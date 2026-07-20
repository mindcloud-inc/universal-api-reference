# Remove Contacts from blacklist with Routee

Removes contacts from the blacklist in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/my/blacklist/:service`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Remove Contacts from blacklist](https://docs.routee.net/reference/remove-contacts-from-blacklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | path | `string` | yes | The service for which the contact will be extracted from blacklist (Sms, TwoStep). |
