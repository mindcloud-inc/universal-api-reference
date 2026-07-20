# Get all issues by URL with SE Ranking Data

Retrieves all issues by URL from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/site-audit/audits/issues`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get all issues by URL](https://seranking.com/api/data/website-audit/#get-all-issues-for-a-specific-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | query | `list<string>` | yes | Audit identifier. |
| `url` | query | `string` | no | Specific URL to fetch issue details for. |
| `url_id` | query | `string` | no | Numeric URL identifier returned by audit pages endpoint. |
