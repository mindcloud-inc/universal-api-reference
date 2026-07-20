# List Inbox Leads with Clio Grow

## Endpoint

- **Method:** `GET`
- **Path:** `/inbox_leads`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [List Inbox Leads](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Inbox-Leads/operation/InboxLead%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_since` | query | `date` | no | Only include inbox leads created on or after this ISO-8601 timestamp. |
| `updated_since` | query | `date` | no | Only include inbox leads updated on or after this ISO-8601 timestamp. |
