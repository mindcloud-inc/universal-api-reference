# Retrieve a list of campaigns created by this book with Routee

Retrieves a list of campaigns created by this book from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:id/campaigns`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve a list of campaigns created by this book](https://docs.routee.net/reference/retrieving-a-list-of-campaigns-created-by-this-book)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID address book |
| `limit` | query | `string` | no | Number of entries (optional parameter) |
| `offset` | query | `string` | no | Offset issue (stating the record to display from) |
