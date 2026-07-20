# List Contacts in Group with DialMyCalls

Retrieves contacts from a specific DialMyCalls group.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:GroupId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [List Contacts in Group](https://www.dialmycalls.com/api-documentation#contacts-get-group)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GroupId` | path | `string` | yes | The DialMyCalls group ID whose contacts should be listed. |
