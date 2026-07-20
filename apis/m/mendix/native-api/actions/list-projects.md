# List Projects with Mendix

Retrieves company-owned projects from Mendix.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [List Projects](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdSince` | query | `date` | no | Only return projects created after this UTC date and time, such as 2020-01-16T05:53:28Z. |
