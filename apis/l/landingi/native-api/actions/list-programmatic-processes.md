# List Programmatic Processes with Landingi

Retrieves programmatic landing page processes from Landingi.

## Endpoint

- **Method:** `GET`
- **Path:** `/landing-page/programmatic/processes`
- **Base URL:** `https://api.landingi.com/v2`
- **Official documentation:** [List Programmatic Processes](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/getProgrammaticLandingPageProcesses)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `object` | no | — |
| `filters[query]` | query | `string` | no | Search by process name. |
| `filters[source_uuid]` | query | `string` | no | Filter by the source landing page UUID. |
