# Merge Leads with Instantly

Merges two leads in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/merge`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Merge Leads](https://developer.instantly.ai/api-reference/lead/merge-two-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | yes | ID of the lead to merge. |
| `destination_lead_id` | body | `string` | yes | ID of the destination lead to merge into. |
