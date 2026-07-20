# Lookup Person with RocketReach

Retrieves a person from RocketReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/person/lookup`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Lookup Person](https://docs.rocketreach.co/reference/people-lookup-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_employer` | query | `string` | no | — |
| `email` | query | `string` | no | — |
| `id` | query | `number` | no | — |
| `linkedin_url` | query | `string` | no | — |
| `lookup_type` | query | `string` | no | Standard, premium, bulk, phone, or enrich lookup mode. |
| `name` | query | `string` | no | — |
| `npi_number` | query | `number` | no | — |
| `return_cached_emails` | query | `boolean` | no | When false, email fields stay null until the lookup completes and verified emails are available from check status or webhooks. |
| `title` | query | `string` | no | — |
| `webhook_id` | query | `number` | no | — |
