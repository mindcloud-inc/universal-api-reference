# Create Lead with Famulor AI - Voice Agent

Creates a new lead in Famulor.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/lead`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Create Lead](https://docs.famulor.io/en/api-reference/leads/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `number` | yes | Campaign ID to create the lead for. |
| `phone_number` | body | `string` | yes | Lead phone number in E.164 format. |
| `variables[]` | body | `array<object>` | no | Optional variables to pass to the lead. |
