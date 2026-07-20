# List Blocked Leads with RoboAuditor

## Endpoint

- **Method:** `GET`
- **Path:** `/blocked_leads`
- **Base URL:** `https://app.siteauditor.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number (starts at 1). |
| `limit` | query | `number` | no | Maximum blocked leads per page. |
| `sort_by` | query | `string` | no | Field to sort by. |
| `sort_desc` | query | `number` | no | Use 1 for descending, 0 for ascending. |
