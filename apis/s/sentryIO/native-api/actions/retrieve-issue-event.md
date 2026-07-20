# Retrieve Issue Event with Sentry IO

Retrieves an event from a Sentry IO issue.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/issues/:issue_id/events/:event_id/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Issue Event](https://docs.sentry.io/api/events/retrieve-an-issue-event/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `issue_id` | path | `string` | yes | The Sentry issue ID. |
| `event_id` | path | `string` | yes | The event ID to retrieve, or latest, oldest, or recommended. |
