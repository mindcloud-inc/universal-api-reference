# Find contacts with Atera

Finds contacts in Atera.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/contacts`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Find contacts](https://app.atera.com/apidocs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchOptions.email` | query | `string` | no | Filter contacts by email address. |
| `searchOptions.phone` | query | `string` | no | Filter contacts by phone number. |
