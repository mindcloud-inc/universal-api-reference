# Get Search Queries with Documenterra

Retrieves search query reports from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/user-events/:prLogin/search-queries`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Get Search Queries](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-poiskovykh-zaprosov)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `date` | yes | ISO 8601 report end timestamp in GMT. |
| `prLogin` | path | `string` | yes | Authorized reader login, or '-' for anonymous users. |
| `projectId` | query | `string` | no | Optional project identifier filter. |
| `startDate` | query | `date` | yes | ISO 8601 report start timestamp in GMT. |
