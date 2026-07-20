# Create Client with ProProfs Project

Creates a new client in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Client](https://help.proprofsproject.com/clients-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_name` | body | `string` | yes | The client name. |
| `email` | body | `string` | no | The client email. |
