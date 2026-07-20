# Get Job Offers with Mona AI

Retrieves job offers from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/database/getJobOffersFromDatabase`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Job Offers](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional job-offer filters such as status, department, and location. |
| `limit` | body | `number` | no | Maximum job offers to return. |
| `page` | body | `number` | no | Page number to retrieve. |
| `sort` | body | `object` | no | Optional sort object with field and direction. |
