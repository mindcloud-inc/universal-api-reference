# Update Link with Linkly

Updates an existing link in Linkly.

## Endpoint

- **Method:** `POST`
- **Path:** `/link`
- **Base URL:** `https://app.linklyhq.com/api/v1`
- **Official documentation:** [Update Link](https://linklyhq.com/support/link-shortening-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Link ID. Required to update an existing link. |
| `url` | body | `string` | no | Optional destination URL. |
| `name` | body | `string` | no | Optional display name for the link. |
| `slug` | body | `string` | no | Optional custom short-code slug. Linkly's current runtime rejects custom slug values in this workspace with `slug must be empty`. |
| `note` | body | `string` | no | Optional internal note for the link. |
| `domain` | body | `string` | no | Optional domain for the link. |
| `enabled` | body | `boolean` | no | Whether the link is enabled. |
| `forward_params` | body | `boolean` | no | Whether to forward query parameters to the destination URL. |
| `hide_referrer` | body | `boolean` | no | Whether to hide the referrer. |
| `cloaking` | body | `boolean` | no | Whether to enable cloaking. |
| `block_bots` | body | `boolean` | no | Whether to block bots. |
| `utm_source` | body | `string` | no | Optional UTM source parameter. |
| `utm_medium` | body | `string` | no | Optional UTM medium parameter. |
| `utm_campaign` | body | `string` | no | Optional UTM campaign parameter. |
| `utm_term` | body | `string` | no | Optional UTM term parameter. |
| `utm_content` | body | `string` | no | Optional UTM content parameter. |
| `rules[]` | body | `array<object>` | no | Optional array of redirect rule objects. Use the nested Rules fields below to define each rule. |
| `rules[].what` | body | `string` | no | What the redirect rule matches against. |
| `rules[].url` | body | `string` | no | Destination URL to use when the rule matches. |
| `rules[].rule_url` | body | `string` | no | Source URL or pattern evaluated by the rule when applicable. |
| `rules[].percentage` | body | `string` | no | Traffic percentage for percentage-based rules. |
| `rules[].matches` | body | `string` | no | Match expression for the redirect rule. |
