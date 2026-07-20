# List Clients with ProProfs Project

Retrieves a list of clients from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Clients](https://help.proprofsproject.com/clients-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_name` | query | `string` | no | Simple wildcard client-name search. |
| `limit` | query | `string` | no | Limit the number of returned clients. |
| `offset` | query | `string` | no | Offset for returned clients. |
