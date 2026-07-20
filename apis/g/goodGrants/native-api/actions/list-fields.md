# List fields with Good Grants

Retrieves fields from Good Grants.

## Endpoint

- **Method:** `GET`
- **Path:** `field`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [List fields](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | query | `string` | no | Filter fields by form slug. |
| `page` | query | `number` | no | Page number greater than 0. |
| `per_page` | query | `number` | no | Results per page, between 1 and 100. |
