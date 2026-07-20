# List Organization Entities with Agicap

Retrieves organization entities for an Agicap organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/organizations/v1/:organizationId/entities`
- **Base URL:** `https://api.agicap.com`
- **Official documentation:** [List Organization Entities](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNumber` | query | `number` | no | Page number to retrieve. Agicap pages start at 1. |
| `pageSize` | query | `number` | no | Number of entities to return per page. |
