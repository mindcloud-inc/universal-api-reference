# Ingest File with Graphor

Creates a new source in Graphor from a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/ingest-file`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Ingest File](https://docs.graphorlm.com/api-reference/sources/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The local file content to upload for ingestion. |
| `method` | body | `string` | no | Optional partition method to use during file ingestion. |
