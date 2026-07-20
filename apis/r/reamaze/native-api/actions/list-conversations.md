# List Conversations with Reamaze

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [List Conversations](https://www.reamaze.com/api/get_conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Conversation scope filter. Supported values include archived, open, unassigned, or all. |
| `archived` | query | `string` | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `open` | query | `string` | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `unassigned` | query | `string` | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `all` | query | `string` | no | `filter` with `archived`, `open`, `unassigned`, or `all` will show only Archived, Open, Unassigned or All conversations, respectively. |
| `for` | query | `string` | no | Return only conversations relevant to the given user email. |
| `email` | query | `string` | no | `for` with a value matching a known user `email` will return only conversations relevant to that user. For example, for a customer user, this would be conversations visible to that customer. |
| `for_id` | query | `string` | no | Return only conversations relevant to the given customer SSO ID. |
| `id` | query | `string` | no | `for_id` with a value matching a known user `id` (from SSO) will return only conversations relevant to that customer user. |
| `sort` | query | `string` | no | Supported values include updated or changed. |
| `updated` | query | `date` | no | `sort` with a value of `updated` will return conversations in descending order of last customer update. A value of `changed` will return conversations in descending order of any update or status change. The default sort order is by conversation `create_at`. |
| `tag` | query | `string` | no | Comma-separated conversation tags to match. |
| `category` | query | `string` | no | Return only conversations from the given channel slug. |
| `data[key]=value` | query | `string` | no | `data` with a hash of key/value pairs (e.g. `data[key]=value`) will return conversations with `data` matching those key/value pairs. |
| `start_date` | query | `date` | no | Filter by latest customer message on or after this ISO 8601 date-time. |
| `end_date` | query | `date` | no | Filter by latest customer message on or before this ISO 8601 date-time. |
| `origin` | query | `string` | no | Filter by conversation origin, for example email, chat, api, instagram, sms, voice, custom, staff, or form. |
