# Update Sender with SuperSend

Updates an existing sender in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/senders/{id}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Sender](https://docs.supersend.io/docs/sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `send_as` | body | `string` | no | — |
| `reply_to` | body | `string` | no | — |
| `signature` | body | `string` | no | — |
| `forward_to` | body | `string` | no | — |
| `forward_rules[]` | body | `array<object>` | no | Per-destination forwarding rules. Each rule maps email destinations to optional label filters. |
| `forward_rules[].emails` | body | `string` | no | Comma-separated email addresses for this rule Send multiple values as a string separated by `,`. |
| `forward_rules[].label_ids[]` | body | `array<string>` | no | — |
| `disabled` | body | `boolean` | no | — |
| `warm` | body | `boolean` | no | — |
| `max_per_day` | body | `number` | no | Range: 1 to 15000. |
| `global_max_per_day` | body | `number` | no | Range: 1 to 1000. |
| `max_warm_per_day` | body | `number` | no | Range: 1 to 1000. |
| `warm_email_ramp` | body | `number` | no | Range: 1 to 365. |
| `campaign_ramp_enabled` | body | `boolean` | no | — |
| `campaign_ramp_duration_days` | body | `number` | no | Days to reach target (required when ramp enabled) Range: 1 to 365. |
| `campaign_ramp_start_volume` | body | `number` | no | Limit on first send day (required when ramp enabled) Range: 1 to inf. |
| `SenderProfileId` | body | `string` | no | — |
