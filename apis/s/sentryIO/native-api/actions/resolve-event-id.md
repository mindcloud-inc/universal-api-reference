# Resolve Event ID with Sentry IO

Resolves a Sentry IO event ID to event details.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/eventids/:event_id/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Resolve Event ID](https://docs.sentry.io/api/organizations/resolve-an-event-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `event_id` | path | `string` | yes | The Sentry event ID to resolve. |
