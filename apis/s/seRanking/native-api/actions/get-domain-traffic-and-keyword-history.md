# Get domain traffic and keyword history with SE Ranking Data

Retrieves domain traffic and keyword history from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/overview/history`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get domain traffic and keyword history](https://seranking.com/api/data/domain-analysis/#history-trends)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to analyze (for example: seranking.com). |
| `month` | query | `list<string>` | no | Optional month number (1-12). Accepted values: `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `source` | query | `string` | yes | Regional database code (for example: us). |
| `year` | query | `string` | yes | Year in YYYY format. |
