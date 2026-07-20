# Retrieve general information about bulk of email address with Routee

Retrieves general information about bulk of email address from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve general information about bulk of email address](https://docs.routee.net/reference/retrieve-general-information-about-bulk-of-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | array of email addresses to retrieve information |
