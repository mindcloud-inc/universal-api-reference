# List Companies with Productlane

Retrieves companies from your Productlane workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [List Companies](https://productlane.mintlify.dev/docs/api/companies/list-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Filter companies by domain. |
| `name` | query | `string` | no | Filter companies by name. |
