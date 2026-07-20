# List Candidates with Polymer

Retrieves candidates from Polymer.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [List Candidates](https://developer.polymer.co/#list-candidates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Exact candidate email address filter. |
