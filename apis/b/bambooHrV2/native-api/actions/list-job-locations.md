# List Job Locations with BambooHR

Lists job locations from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/hris/org/locations`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Job Locations](https://documentation.bamboohr.com/reference/get-locations)

## Requirements

- **OAuth scopes:** `field`
- **scope:** `field` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Ordering by OData (Open Data Protocol) v4 specification. Supported fields: label, archived, manageable, address/address1, address/address2, address/city, address/stateId, address/zipcode, address/countryId, address/timezone, address/remoteLocation, createdAt, archivedAt |
| `select` | query | `string` | no | Projection (field selection) by OData specification. Supported fields: id, label, archived, manageable, address/address1, address/address2, address/city, address/stateId, address/zipcode, address/countryId, address/timezone, address/remoteLocation, createdAt, archivedAt |
| `filter` | query | `string` | no | Filter by an OData (Open Data Protocol) v4 specification. Supported fields: id, label, archived, manageable, address/address1, address/address2, address/city, address/stateId, address/zipcode, address/countryId, address/timezone, address/remoteLocation |
| `expand` | query | `list<string>` | no | Comma-separated list of related resources to expand. Supported values: state, country. Example: expand=state,country Accepted values: `country`, `state`. Send multiple values as a string separated by `,`. |
