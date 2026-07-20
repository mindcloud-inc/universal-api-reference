# List Latest News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/latest`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [List Latest News](https://newsdata.io/documentation#latest-news)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Category filter for latest news results. |
| `country` | query | `string` | no | Country code filter for latest news results. |
| `domainurl` | query | `string` | no | Filter latest news by one or more source domain URLs. |
| `language` | query | `string` | no | Language code filter for latest news results. |
| `q` | query | `string` | no | Keyword or phrase to search for in latest news results. |
