# Retrieve information for list of emails with Routee

Retrieves information for list of emails from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/smtp/emails/info`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve information for list of emails](https://docs.routee.net/reference/retrieving-information-for-list-of-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | query | `array<string>` | no | array of message ID's, max 500 per request |
