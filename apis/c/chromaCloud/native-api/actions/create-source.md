# Create source with Chroma Cloud

Creates a source in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `https://sync.trychroma.com/api/v1/sources`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Create source](https://docs.trychroma.com/reference/sync-api/source/create-source)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `database_name` | body | `string` | yes |
| `github` | body | `object` | no |
| `web_scrape` | body | `object` | no |
| `s3` | body | `object` | no |
| `chunking` | body | `object` | no |
| `embedding` | body | `object` | no |
