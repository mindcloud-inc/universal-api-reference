# Get Contacts with Alto

Retrieves contacts from Alto by IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Contacts](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | One or more Alto contact identifiers. Send multiple values as a string separated by `,`. |
