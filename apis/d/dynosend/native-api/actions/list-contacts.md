# List Contacts with Dynosend

Retrieves contacts from Dynosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [List Contacts](https://developers.dynosend.com/#listcontacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | query | `string` | yes | The UID of the audience whose contacts you want to list. |
