# Retrieve Issue with Sentry IO

Retrieves an issue from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/issues/:issue_id/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Issue](https://docs.sentry.io/api/events/retrieve-an-issue/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `issue_id` | path | `string` | yes | The Sentry issue ID. |
