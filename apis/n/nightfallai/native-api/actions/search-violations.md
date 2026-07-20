# Search Violations with Nightfall.ai

Finds violations in Nightfall.ai by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/dlp/v1/violations/search`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Search Violations](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Nightfall search query string, for example state:pending. |
| `sort` | query | `list` | no | Optional sort order such as TIME_DESC, TIME_ASC, RELEVANCE, RISK_ASC, or RISK_DESC. Accepted values: `Relevance`, `Risk Asc`, `Risk Desc`, `Time Asc`, `Time Desc`. |
