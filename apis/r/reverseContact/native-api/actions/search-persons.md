# Search Persons with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/search/persons`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Search Persons](https://app.reversecontact.com/docs/endpoints/search-persons)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currentCompanyName` | body | `string` | no | Filter by the person's current company name. |
| `currentPositionTitle` | body | `string` | no | Filter by the person's current job title. |
