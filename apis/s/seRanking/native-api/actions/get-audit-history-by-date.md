# Get audit history by date with SE Ranking Data

Retrieves audit history by date from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/site-audit/audits/history`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get audit history by date](https://seranking.com/api/data/website-audit/#get-audit-history-by-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | query | `list<string>` | yes | Audit identifier. |
| `date` | query | `string` | yes | Date for history retrieval (YYYY-MM-DD). |
