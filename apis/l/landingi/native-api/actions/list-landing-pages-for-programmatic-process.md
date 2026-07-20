# List Landing Pages for Programmatic Process with Landingi

Retrieves landing pages for a Landingi programmatic process.

## Endpoint

- **Method:** `GET`
- **Path:** `/landing-page/programmatic/processes/:processUuid/landing-pages`
- **Base URL:** `https://api.landingi.com/v2`
- **Official documentation:** [List Landing Pages for Programmatic Process](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/getProgrammaticLandingPageProcessLandingPages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processUuid` | path | `string` | yes | Programmatic process UUID. |
| `filters` | query | `object` | no | — |
| `filters[query]` | query | `string` | no | Search by landing page name or assigned URL. |
| `filters[status]` | query | `string` | no | Filter by landing page status. |
