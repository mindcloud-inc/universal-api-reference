# Create Company with Agile CRM

Creates a new company in Agile CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Create Company](https://github.com/agilecrm/rest-api#21-creating-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `url` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `lead_score` | body | `number` | no | Lead score value for the company record. |
| `star_value` | body | `number` | no | Star value for company prioritization. |
