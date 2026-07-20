# List Stories by UUIDs with Storyblok

Retrieves Storyblok stories for specific UUIDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories by UUIDs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by_uuids` | query | `string` | yes | A comma-separated list of story UUIDs to return. |
