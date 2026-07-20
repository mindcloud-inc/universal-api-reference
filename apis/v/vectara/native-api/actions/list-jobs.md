# List Jobs with Vectara

Retrieves background job records from Vectara.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/jobs`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [List Jobs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of jobs to return. |
| `page_key` | query | `string` | no | Cursor for the next page of jobs. |
