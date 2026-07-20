# List Stories in Workflow Stage with Storyblok

Retrieves Storyblok stories in specific workflow stages.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories in Workflow Stage](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `in_workflow_stages` | query | `string` | yes | A comma-separated list of workflow stage IDs to filter by. |
