# Update Campaign with SuperSend

Updates an existing campaign in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/{id}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Campaign](https://docs.supersend.io/docs/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `name` | body | `string` | no | — |
| `track_domain` | body | `string` | no | — |
| `track` | body | `boolean` | no | — |
| `nodes[]` | body | `array` | no | — |
| `edges[]` | body | `array` | no | — |
| `status` | body | `number` | no | Allowed values: 1, 2. |
| `is_draft` | body | `boolean` | no | — |
| `timezone` | body | `string` | no | — |
| `days` | body | `object` | no | — |
| `hours[]` | body | `array<object>` | no | — |
| `hours[].start` | body | `string` | no | — |
| `hours[].end` | body | `string` | no | — |
| `start` | body | `date` | no | — |
| `end` | body | `date` | no | — |
| `bcc[]` | body | `array<string>` | no | — |
| `bcc_replies_only` | body | `boolean` | no | — |
| `unsubscribe` | body | `boolean` | no | — |
| `unsubscribe_message` | body | `string` | no | — |
| `blacklistIfUnsubscribe` | body | `boolean` | no | — |
| `blacklistIfBounced` | body | `boolean` | no | — |
| `blacklistDomainOnReply` | body | `boolean` | no | — |
| `list_unsubscribe_header` | body | `boolean` | no | — |
| `failureConfiguration` | body | `object` | no | — |
| `failureConfiguration.strategy` | body | `string` | no | Allowed values: skip, retry, pause_contact, pause_campaign. |
| `failureConfiguration.retryAfterDays` | body | `number` | no | — |
| `failureConfiguration.notification` | body | `boolean` | no | — |
| `send_to_risk_levels[]` | body | `array<string>` | no | — |
| `max_per_day` | body | `number` | no | — |
