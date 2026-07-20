# List Market News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/market`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [List Market News](https://newsdata.io/documentation#market-news)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Country code filter for market news results. |
| `language` | query | `string` | no | Language code filter for market news results. |
| `q` | query | `string` | no | Keyword or phrase to search for in market news results. |
