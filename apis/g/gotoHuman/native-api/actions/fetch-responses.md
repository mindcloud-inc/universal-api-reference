# Fetch Responses with gotoHuman

Retrieves past review responses from gotoHuman.

## Endpoint

- **Method:** `GET`
- **Path:** `/fetchResponses`
- **Base URL:** `https://api.gotohuman.com`
- **Official documentation:** [Fetch Responses](https://docs.gotohuman.com/agent-memory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | yes | The ID of the review template / form. |
| `fieldIds` | query | `string` | yes | Comma-separated field IDs to fetch. |
| `filterResponse` | query | `string` | no | Filter by review status: approved or rejected. |
| `filterResponseValues` | query | `string` | no | URL-encoded JSON string array used to filter response values. |
| `groupByField` | query | `boolean` | no | Whether to group the responses by field. |
| `approvedValuesOnly` | query | `boolean` | no | Return only approved values. |
| `rejectedValuesOnly` | query | `boolean` | no | Return only rejected values. |
| `limit` | query | `number` | no | Maximum number of responses to return. |
