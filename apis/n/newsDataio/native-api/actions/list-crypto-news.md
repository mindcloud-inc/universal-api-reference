# List Crypto News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/crypto`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [List Crypto News](https://newsdata.io/documentation#crypto-news)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Country code filter for crypto news results. |
| `language` | query | `string` | no | Language code filter for crypto news results. |
| `q` | query | `string` | no | Keyword or phrase to search for in crypto news results. |
