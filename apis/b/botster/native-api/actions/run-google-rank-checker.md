# Run Google Rank Checker with Botster

Creates a Botster Google rank checking job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-rank-checker`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Google Rank Checker](https://botster.io/bots/google-rank-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Search queries. |
| `coordinates` | body | `object` | yes | Location coordinates. |
| `language` | body | `string` | yes | Language. |
| `device` | body | `list` | yes | Device type. Accepted values: `Desktop`, `Mobile`. |
| `os` | body | `string` | yes | Operating system. |
| `domain` | body | `string` | yes | Domain to compare. |
| `cron` | body | `string` | no | Cron expression for periodic runs. |
| `new_items_only` | body | `boolean` | no | Return only items that appeared since the latest crawl. |
