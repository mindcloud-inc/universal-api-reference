# List Jobs with Polymer

Retrieves jobs from Polymer.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [List Jobs](https://developer.polymer.co/#list-jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by job status: published, draft, archived, or public. |
