# Update Campaign Status with Famulor AI - Voice Agent

Starts, pauses, or stops a campaign in Famulor.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/campaigns/update-status`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Update Campaign Status](https://docs.famulor.io/en/api-reference/campaigns/update-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `number` | yes | Campaign ID to update. |
| `status` | body | `string` | yes | New campaign status. |
