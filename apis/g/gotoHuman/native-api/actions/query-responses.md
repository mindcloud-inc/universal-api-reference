# Query Responses with gotoHuman

## Endpoint

- **Method:** `GET`
- **Path:** `/queryResponses`
- **Base URL:** `https://api.gotohuman.com`
- **Official documentation:** [Query Responses](https://docs.gotohuman.com/training-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | yes | The ID of the review template / form. |
| `fieldIds` | query | `string` | yes | Comma-separated field IDs to query. |
| `filterResponse` | query | `string` | no | Filter by review status: approved or rejected. |
| `groupByField` | query | `boolean` | no | Whether to group the responses by field. |
| `approvedValuesOnly` | query | `boolean` | no | Return only approved values. |
| `rejectedValuesOnly` | query | `boolean` | no | Return only rejected values. |
| `limit` | query | `number` | no | Maximum number of responses to return. |
