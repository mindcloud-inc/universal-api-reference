# Search Mission Critical Jobs with USAJOBS

Finds mission critical jobs in USAJOBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Mission Critical Jobs](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MissionCriticalTags` | query | `string` | no | Mission critical grouping tag, such as STEM. |
