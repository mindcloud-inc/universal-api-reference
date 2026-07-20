# List Meetings with Fathom

Retrieves meetings from Fathom.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings`
- **Base URL:** `https://api.fathom.ai/external/v1`
- **Official documentation:** [List Meetings](https://developers.fathom.ai/api-reference/meetings/list-meetings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor for pagination. |
| `created_after` | query | `date` | no | Filter meetings created after this timestamp (ISO 8601). |
| `created_before` | query | `date` | no | Filter meetings created before this timestamp (ISO 8601). |
| `teams[]` | query | `string` | no | Filter by one or more team names. Send multiple values as a array. |
| `recorded_by[]` | query | `string` | no | Filter by one or more recorder email addresses. Send multiple values as a array. |
| `calendar_invitees_domains[]` | query | `string` | no | Filter by invitee domains. Pass one value per domain. Send multiple values as a array. |
| `calendar_invitees_domains_type` | query | `string` | no | all, only_internal, or one_or_more_external. |
| `include_action_items` | query | `boolean` | no | Include action items for each meeting. |
| `include_crm_matches` | query | `boolean` | no | Include CRM matches for each meeting. |
