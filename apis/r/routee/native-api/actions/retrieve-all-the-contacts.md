# Retrieve all the contacts with Routee

Retrieves all the contacts from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve all the contacts](https://docs.routee.net/reference/retrieve-all-the-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. Max value: 2000 |
