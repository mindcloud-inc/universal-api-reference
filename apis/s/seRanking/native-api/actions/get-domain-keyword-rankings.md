# Get Domain Keyword Rankings with SE Ranking Data

Retrieves domain keyword rankings from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/keywords`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get Domain Keyword Rankings](https://seranking.com/api/data/domain-analysis/#domain-keywords)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | yes | Database region code (for example: us). |
| `domain` | query | `string` | yes | Domain to retrieve ranking keywords for (for example: seranking.com). |
