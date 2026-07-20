# Get Page Views with Documenterra

Retrieves page view reports from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/user-events/:prLogin/articles`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Get Page Views](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-prosmotrov-stranitsy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `date` | yes | ISO 8601 report end timestamp in GMT. |
| `prLogin` | path | `string` | yes | Authorized reader login, or '-' for anonymous users. |
| `startDate` | query | `date` | yes | ISO 8601 report start timestamp in GMT. |
