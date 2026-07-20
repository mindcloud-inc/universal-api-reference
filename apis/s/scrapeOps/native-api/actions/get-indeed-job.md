# Get Indeed Job with ScrapeOps

Retrieves Indeed job details from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/indeed/job-detail`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Get Indeed Job](https://scrapeops.io/docs/data-api/indeed-job-detail-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | — |
| `job_id` | query | `string` | no | Indeed job ID to fetch. |
| `tld` | query | `string` | no | — |
| `url` | query | `string` | no | Full Indeed job URL to fetch. |
