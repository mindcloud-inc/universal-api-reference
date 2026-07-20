# List Archive Shows By Date with All Things Considered Podcast

Retrieves archived shows by date from All Things Considered Podcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/all-things-considered/archive`
- **Base URL:** `https://www.npr.org`
- **API:** rest
- **Official documentation:** [List Archive Shows By Date](https://www.npr.org/programs/all-things-considered/archive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Archive date to load, formatted as YYYY-MM-DD. |
