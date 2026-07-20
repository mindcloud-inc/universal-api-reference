# Update Lead Interest Status with Instantly

Updates a lead interest status in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/update-interest-status`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Lead Interest Status](https://developer.instantly.ai/api-reference/lead/update-the-interest-status-of-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_email` | body | `string` | yes | Email of the lead to update. |
| `interest_value` | body | `number` | yes | Interest status value to set. |
