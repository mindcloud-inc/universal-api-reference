# Get audit pages by issue with SE Ranking Data

Retrieves audit pages by issue from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/site-audit/audits/issue-pages`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get audit pages by issue](https://seranking.com/api/data/website-audit/#get-audit-pages-by-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | query | `list<string>` | yes | Audit identifier. |
| `code` | query | `string` | yes | Issue code filter. |
