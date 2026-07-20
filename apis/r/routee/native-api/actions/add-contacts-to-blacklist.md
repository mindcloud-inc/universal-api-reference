# Add contacts to blacklist with Routee

Adds contacts to the blacklist in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/my/blacklist/:service`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Add contacts to blacklist](https://docs.routee.net/reference/add-contacts-to-blacklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | path | `string` | yes | The service (Sms, Voice, Viber, TwoStep, Lookup, NumberValidator) for which the contact will be added in blacklist. |
| `contacts[]` | body | `array<string>` | yes | The contacts' ids. |
