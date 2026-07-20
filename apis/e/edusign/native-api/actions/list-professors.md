# List Professors with Edusign

Retrieves professors from Edusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/professor`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [List Professors](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | yes | Query param for pagination, starts at page "0" and displays 100 professors per page |
