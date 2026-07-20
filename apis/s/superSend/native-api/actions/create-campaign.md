# Create Campaign with SuperSend

Creates a new campaign in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Create Campaign](https://docs.supersend.io/docs/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `TeamId` | body | `string` | yes | — |
| `track_domain` | body | `string` | no | Tracking domain for links (team default used if omitted) |
| `nodes[]` | body | `array` | no | — |
| `edges[]` | body | `array` | no | — |
| `is_draft` | body | `boolean` | no | Default: true. |
| `version` | body | `number` | no | Allowed values: 1, 2, 3. Default: 2. |
| `custom_variables[]` | body | `array<object>` | no | — |
| `custom_variables[].name` | body | `string` | no | — |
| `custom_variables[].type` | body | `string` | no | Allowed values: text, boolean. Default: text. |
| `templateId` | body | `string` | no | — |
| `track` | body | `boolean` | no | Enable open and click tracking. When false, no pixels or link rewrites. |
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
| `blacklistIfUnsubscribe` | body | `boolean` | no | Default: true. |
| `blacklistIfBounced` | body | `boolean` | no | Default: true. |
| `blacklistDomainOnReply` | body | `boolean` | no | Default: true. |
| `list_unsubscribe_header` | body | `boolean` | no | — |
| `failureConfiguration` | body | `object` | no | — |
| `failureConfiguration.strategy` | body | `string` | no | Allowed values: skip, retry, pause_contact, pause_campaign. |
| `failureConfiguration.retryAfterDays` | body | `number` | no | — |
| `failureConfiguration.notification` | body | `boolean` | no | — |
| `send_to_risk_levels[]` | body | `array<string>` | no | — |
