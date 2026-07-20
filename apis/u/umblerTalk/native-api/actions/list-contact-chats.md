# List Contact Chats with Umbler Talk

Retrieves a contact's chats from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/[:id]/chats/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Contact Chats](https://app-utalk.umbler.com/api/docs/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The contact ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
