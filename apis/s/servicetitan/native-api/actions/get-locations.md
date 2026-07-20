# Get Locations with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/locations`
- **Base URL:** `https://{baseUrl}/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Perform lookup by multiple IDs (maximum 50) |
| `customerId` | query | `number` | no | — |
| `name` | query | `string` | no | — |
| `street` | query | `string` | no | — |
| `unit` | query | `string` | no | — |
| `city` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `zip` | query | `string` | no | — |
| `country` | query | `string` | no | — |
| `latitude` | query | `string` | no | — |
| `longitude` | query | `string` | no | — |
| `includeTotal` | query | `boolean` | no | — |
| `externalDataKey` | query | `string` | no | — |
| `externalDataValues` | query | `string` | no | — |
| `pageSize` | query | `number` | no | — |
| `page` | query | `number` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `externalDataApplicationGuid` | query | `string` | no | — |
