# List Contacts with Quo

Retrieves all contacts from Quo.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [List Contacts](https://www.quo.com/docs/mdx/api-reference/contacts/list-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `externalIds[]` | query | `array<string>` | no |
| `sources[]` | query | `array<string>` | no |
