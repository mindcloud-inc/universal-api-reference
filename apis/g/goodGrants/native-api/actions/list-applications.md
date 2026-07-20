# List applications with Good Grants

Retrieves applications from Good Grants.

## Endpoint

- **Method:** `GET`
- **Path:** `application`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [List applications](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | query | `string` | no | Filter applications by form slug. |
| `page` | query | `number` | no | Page number greater than 0. |
| `per_page` | query | `number` | no | Results per page, between 1 and 100. |
