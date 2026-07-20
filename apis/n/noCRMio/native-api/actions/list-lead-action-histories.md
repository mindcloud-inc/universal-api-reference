# List Lead Action Histories with noCRM.io

Retrieves lead action histories from noCRM.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/:lead_id/action_histories`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [List Lead Action Histories](https://www.nocrm.io/api#list-the-action-histories-on-a-lead)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Lead ID. |
| `from` | query | `date` | no | Start date for the history range. |
| `to` | query | `date` | no | End date for the history range. |
| `action_type` | query | `string` | no | Filter by action type. |
| `action_value` | query | `string` | no | Filter by action value. |
| `user_ids` | query | `list<string>` | no | Comma-separated user IDs or emails. Send multiple values as a string separated by `,`. |
| `direction` | query | `string` | no | Sort direction for returned history. |
