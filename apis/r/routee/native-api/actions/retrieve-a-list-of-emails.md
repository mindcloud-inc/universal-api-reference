# Retrieve a list of emails with Routee

Retrieves a list of emails from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/smtp/emails`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve a list of emails](https://docs.routee.net/reference/retrieving-a-list-of-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Number of entries |
| `offset` | query | `string` | no | Sample offset |
| `from` | query | `string` | no | Sample start date |
| `to` | query | `string` | no | Sample max date |
| `sender` | query | `string` | no | Sender |
| `recipient` | query | `string` | no | Recipient |
