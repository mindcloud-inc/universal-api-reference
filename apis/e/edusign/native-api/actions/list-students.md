# List Students with Edusign

Retrieves students from Edusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/student`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [List Students](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | Query param for pagination, starts at page "0" |
| `limit` | query | `string` | no | Number of students per page |
| `updatedAfter` | query | `string` | no | Filter students updated after this date (ISO format) |
| `search` | query | `string` | no | Search in student's firstname, lastname and email |
