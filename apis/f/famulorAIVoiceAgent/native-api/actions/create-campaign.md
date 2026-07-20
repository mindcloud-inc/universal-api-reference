# Create Campaign with Famulor AI - Voice Agent

Creates a new outbound campaign in Famulor.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/campaign`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Create Campaign](https://docs.famulor.io/en/api-reference/campaigns/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | body | `number` | yes | Assistant ID assigned to the campaign. |
| `name` | body | `string` | yes | Campaign name. |
