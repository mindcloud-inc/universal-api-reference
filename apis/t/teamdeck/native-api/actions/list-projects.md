# List Projects with Teamdeck

Retrieves projects from your Teamdeck organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [List Projects](https://teamdeck.io/developers/api#operation/projectsList)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields` | query | `string` | no |
| `expand` | query | `string` | no |
| `name` | query | `string` | no |
| `archived` | query | `number` | no |
