# Recheck standard audit with SE Ranking Data

Rechecks a standard audit in SE Ranking Data.

## Endpoint

- **Method:** `POST`
- **Path:** `/site-audit/audits/recheck/standard`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Recheck standard audit](https://seranking.com/api/data/website-audit/#recheck-audit-standard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | query | `list<string>` | yes | Audit identifier. |
