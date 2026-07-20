# Ingest GitHub Repository with Graphor

Creates a new source in Graphor from a GitHub repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/ingest-github`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Ingest GitHub Repository](https://docs.graphorlm.com/api-reference/sources/upload#ingest-github)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The GitHub repository URL to ingest. |
