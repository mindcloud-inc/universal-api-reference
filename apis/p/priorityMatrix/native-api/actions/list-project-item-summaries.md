# List Project Item Summaries with Priority Matrix

Retrieves item summaries from a Priority Matrix project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/project/:idd/item_summaries/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [List Project Item Summaries](https://sync.appfluence.com/developer/guide/#common-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idd` | path | `number` | yes | Project IDD. |
