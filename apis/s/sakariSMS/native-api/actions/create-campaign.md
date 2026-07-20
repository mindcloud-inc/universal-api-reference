# Create Campaign with Sakari SMS

Creates a new campaign in Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/campaigns`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Create Campaign](https://developer.sakari.io/api-reference/campaigns/create-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `trigger` | body | `object` | no | — |
| `trigger.code` | body | `string` | no | Campaign type specifies how it sources contacts and what event triggers its execution  Sort order   * `M` - Manual   * `S` - Scheduled   * `FU` - File Upload   * `V2` - V2 |
| `filters` | body | `object` | no | — |
| `filters.contacts[]` | body | `array<string>` | no | — |
| `filters.tags[]` | body | `array<string>` | no | — |
| `filters.attributes[]` | body | `array<string>` | no | — |
| `template` | body | `string` | no | — |
| `reporting` | body | `object` | no | — |
| `reporting.when` | body | `string` | no | — |
