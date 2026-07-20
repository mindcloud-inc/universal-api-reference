# List Conversations with Missive

Retrieves conversations from your Missive workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [List Conversations](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of conversations returned. Default 25, max 50. |
| `until` | query | `number` | no | Unix timestamp used to paginate with the oldest conversation last_activity_at value from the previous page. |
| `inbox` | query | `boolean` | no | Pass true to list conversations in the Inbox mailbox. |
| `all` | query | `boolean` | no | Pass true to list conversations in the All mailbox. |
| `assigned` | query | `boolean` | no | Pass true to list conversations assigned to the token owner. |
| `closed` | query | `boolean` | no | Pass true to list conversations in Closed. |
| `snoozed` | query | `boolean` | no | Pass true to list conversations in Snoozed. |
| `flagged` | query | `boolean` | no | Pass true to list conversations in Starred. |
| `trashed` | query | `boolean` | no | Pass true to list conversations in Trash. |
| `junked` | query | `boolean` | no | Pass true to list conversations in Spam. |
| `drafts` | query | `boolean` | no | Pass true to list conversations in Drafts. |
| `shared_label` | query | `string` | no | Shared label ID to filter conversations in that shared label. |
| `team_inbox` | query | `string` | no | Team ID to list conversations in the team's Inbox mailbox. |
| `team_closed` | query | `string` | no | Team ID to list conversations in the team's Closed mailbox. |
| `team_all` | query | `string` | no | Team ID to list conversations in the team's All mailbox. |
| `organization` | query | `string` | no | Organization ID to restrict conversations shared with the organization. |
| `email` | query | `string` | no | Specific contact email address filter. Mutually exclusive with Domain and Contact Organization. |
| `domain` | query | `string` | no | Specific contact email domain filter. Mutually exclusive with Email and Contact Organization. |
| `contact_organization` | query | `string` | no | Contact organization or group UUID filter. Mutually exclusive with Email and Domain. |
