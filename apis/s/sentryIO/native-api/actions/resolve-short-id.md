# Resolve Short ID with Sentry IO

Retrieves Sentry IO issue details by short ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/shortids/:issue_id/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Resolve Short ID](https://docs.sentry.io/api/organizations/resolve-a-short-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `issue_id` | path | `string` | yes | The short issue ID to resolve, such as PROJECT-123. |
