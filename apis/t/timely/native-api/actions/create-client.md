# Create Client with Timely

Creates a client in Timely.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.1/{account_id}/clients`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Create Client](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID for the client you want to create |
| `client` | body | `object` | yes | — |
