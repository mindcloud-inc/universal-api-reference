# List Questionnaires with snapADDY

## Endpoint

- **Method:** `GET`
- **Path:** `/visitreport/v1/backend/questionnaires/all`
- **Base URL:** `https://api.snapaddy.com`
- **Official documentation:** [List Questionnaires](https://developers.snapaddy.com/visitreport-rest-api/reference/questionnaires)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of questionnaires to return |
| `page` | query | `number` | no | Page number |
| `finalizedOnly` | query | `boolean` | no | Filter for finalized questionnaires only |
| `order` | query | `string` | no | Sort order expression |
| `filter` | query | `string` | no | Filter expression |
| `search` | query | `string` | no | Search term |
