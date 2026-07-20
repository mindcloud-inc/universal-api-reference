# Update Issue with Sentry IO

Updates an existing issue in Sentry IO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:organization_id_or_slug/issues/:issue_id/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Update Issue](https://docs.sentry.io/api/events/update-an-issue/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `issue_id` | path | `string` | yes | The Sentry issue ID to update. |
| `status` | body | `list` | no | New issue status: resolved, resolvedInNextRelease, unresolved, or ignored. Accepted values: `0`, `1`, `2`, `3`. |
| `assignedTo` | body | `string` | no | Actor ID or username of the user or team to assign to the issue. |
| `isBookmarked` | body | `boolean` | no | Whether the invoking user has bookmarked the issue. |
| `isSubscribed` | body | `boolean` | no | Whether the invoking user is subscribed to issue notifications. |
