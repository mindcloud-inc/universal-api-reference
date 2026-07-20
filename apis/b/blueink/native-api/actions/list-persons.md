# List Persons with Blueink

Retrieves persons from your Blueink account.

## Endpoint

- **Method:** `GET`
- **Path:** `/persons/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [List Persons](https://developer.blueink.com/api/#tag/Person/operation/listPersons)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search by name, email, or phone. |
| `email` | query | `string` | no | Filter persons by email address. |
| `phone` | query | `string` | no | Filter persons by phone number. |
