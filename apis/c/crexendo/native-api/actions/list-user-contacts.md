# List User Contacts with Crexendo

Retrieves contacts for a user in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/users/:user/contacts`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List User Contacts](https://docs.ns-api.com/reference/get_domains-domain-users-user-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
| `user` | path | `string` | yes | User extension or identifier, for example 1000. |
