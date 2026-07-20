# List Person Deals with Teamgate

Retrieves deals for a person in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/{{personId}}/deals`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [List Person Deals](https://developers.teamgate.com/#c6e6df8c-e097-4d8a-b060-2d2b5d08fde4)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | Person ID whose deals should be listed. |
