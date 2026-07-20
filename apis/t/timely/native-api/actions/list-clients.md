# List Clients with Timely

Retrieves clients from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/clients`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Clients](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID for the clients you want to retrieve |
| `limit` | query | `number` | no | Retrieve number of clients |
| `order` | query | `string` | no | "asc (default)" and "desc" |
| `offset` | query | `number` | no | Retrieve clients from offset |
| `show` | query | `string` | no | Specifies which records to retrieve. Example: "show=all" or "show=active" or "show=archived" |
