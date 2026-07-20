# Search Jobs with Datastreamer

Finds jobs in Datastreamer by Lucene query.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/jobs/search`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Search Jobs](https://docs.datastreamer.io/docs/searching-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Search request payload. |
| `query.query` | body | `string` | yes | Lucene query string used to search job history. |
| `query.from` | body | `number` | no | Zero-based starting offset for the search results. |
| `query.size` | body | `number` | no | Maximum number of jobs to return. |
| `query.track_total_hits` | body | `boolean` | no | Return the total number of matching jobs. |
| `query.sort[]` | body | `array<object>` | no | Sort instructions for the search. |
| `query.sort[].field` | body | `string` | no | Job field used for sorting. |
| `query.sort[].order` | body | `string` | no | Sort order, ASC or DESC. |
