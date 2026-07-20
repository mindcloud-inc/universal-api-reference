# List Projects with CompanyCam

Retrieves a list of projects from CompanyCam.

## Endpoint

- **Method:** `GET`
- **Path:** `projects`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [List Projects](https://docs.companycam.com/reference/listprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | An optional value to filter the projects by name or address line 1 |
| `modified_since` | query | `string` | no | — |
