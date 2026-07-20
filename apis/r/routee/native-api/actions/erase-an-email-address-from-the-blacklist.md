# Erase an email address from the blacklist with Routee

Deletes an email address from the blacklist in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/blacklist`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Erase an email address from the blacklist](https://docs.routee.net/reference/erasing-an-email-address-from-the-blacklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `string` | yes | A string containing email addresses separated by commas encoded in base64 |
