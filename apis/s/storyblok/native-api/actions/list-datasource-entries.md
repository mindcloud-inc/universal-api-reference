# List Datasource Entries with Storyblok

Retrieves datasource entries from Storyblok by datasource.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasource_entries`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Datasource Entries](https://www.storyblok.com/docs/api/content-delivery/v2/datasource-entries/retrieve-multiple-datasource-entries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasource` | query | `string` | yes | The datasource slug to read entries from. |
