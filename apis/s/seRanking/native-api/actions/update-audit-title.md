# Update audit title with SE Ranking Data

Updates an audit title in SE Ranking Data.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/site-audit/audits`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Update audit title](https://seranking.com/api/data/website-audit/#update-audit-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | query | `list<string>` | yes | Audit identifier. |
| `title` | body | `string` | yes | New audit title. |
