# List Trainings with Edusign

Retrieves trainings from Edusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/trainings/`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [List Trainings](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | yes | Query param for pagination, starts at page "0" and displays 50 trainings per page |
| `name` | query | `string` | no | Filter trainings based on their name |
| `date` | query | `string` | no | An array of two dates (start and end) to filter the dates of the training |
| `students` | query | `string` | no | Filter trainings based on an array of students ids enrolled in that training |
| `professors` | query | `string` | no | An array of professors IDs to filter the professors ids of the training |
| `archived` | query | `string` | no | Filters the archived status of the training |
| `creatorId` | query | `string` | no | An array of creator IDs to filter the creator of the training |
| `dateCreated` | query | `string` | no | An array of two dates (start and end) to filter the date created of the training |
| `dateUpdated` | query | `string` | no | An array of two dates (start and end) to filter the date updated of the training |
