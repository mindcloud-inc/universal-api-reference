# List Contact Lists with Wooxy

Finds contact lists in your Wooxy account.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contact-list/find`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [List Contact Lists](https://wooxy.com/api-documentation/contact-list/find-contact-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | no | Contact list ID in Wooxy. |
| `contactListName` | body | `string` | no | Contact list name in Wooxy. |
| `domain` | body | `string` | no | Verified sender domain in Wooxy. |
| `domainId` | body | `string` | no | Unique Wooxy domain ID. |
