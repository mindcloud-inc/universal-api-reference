# Retrieve a list of emails from a mailing list with Routee

Retrieves a list of emails from a mailing list in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:id/emails`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve a list of emails from a mailing list](https://docs.routee.net/reference/retrieving-a-list-of-emails-from-a-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | List ID |
| `limit` | body | `number` | no | number of entries |
| `offset` | body | `string` | no | offset (stating the first record to display) |
