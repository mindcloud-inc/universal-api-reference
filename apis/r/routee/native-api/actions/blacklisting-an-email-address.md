# Blacklisting an email address with Routee

Adds an email address to the Routee blacklist.

## Endpoint

- **Method:** `POST`
- **Path:** `/blacklist`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Blacklisting an email address](https://docs.routee.net/reference/blacklisting-an-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | query | `string` | yes | A string containing email addresses separated by commas encoded in base64 |
| `comment` | query | `string` | no | A comment encoded in base64 (an optional parameter) |
