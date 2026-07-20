# List Contacts with AMcards.com

Retrieves contact records from your AMcards.com account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Contacts](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groups__id` | query | `number` | no | Filter contacts to a specific group. |
