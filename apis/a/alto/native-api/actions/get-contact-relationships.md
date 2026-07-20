# Get Contact Relationships with Alto

Retrieves contact relationships from Alto by contact ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contactId/relationship`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Contact Relationships](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Unique Alto contact identifier. |
| `relationshipType` | query | `string` | no | Relationship type filter. |
