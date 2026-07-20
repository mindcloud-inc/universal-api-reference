# Get Job Title Suggestions with Prospeo

Finds job title suggestions in Prospeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/search-suggestions`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Get Job Title Suggestions](https://prospeo.io/api-docs/search-suggestions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_title_search` | body | `string` | yes | Search query to find job title suggestions. Minimum 2 characters. |
