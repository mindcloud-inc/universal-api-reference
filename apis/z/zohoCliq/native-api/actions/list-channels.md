# List Channels with Zoho Cliq

Retrieves Zoho Cliq channels by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Channels](https://www.zoho.com/cliq/help/restapi/v2/#Channels_List_all_channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter channels by name. |
| `status` | query | `string` | no | Filter channels by status: created, pending, or archived. |
| `limit` | query | `number` | no | The number of channels to retrieve. Maximum 100. |
| `level` | query | `string` | no | Filter channels by level: organization, team, private, or external. |
| `modified_before` | query | `string` | no | Only include channels whose last message was sent before this time. |
| `modified_after` | query | `string` | no | Only include channels whose last message was sent after this time. |
| `created_before` | query | `string` | no | Only include channels created before this time. |
| `created_after` | query | `string` | no | Only include channels created after this time. |
| `channel_ids` | query | `string` | no | Comma-separated channel IDs to retrieve. |
| `chat_ids` | query | `string` | no | Comma-separated channel chat IDs to retrieve. |
| `team_ids` | query | `string` | no | Comma-separated team IDs whose channels should be retrieved. |
| `created_by` | query | `string` | no | Filter channels by creator email or user ID. |
| `order_by` | query | `string` | no | Sort channels by last modified or creation time. |
| `next_token` | query | `string` | no | Use the next token from a previous response to retrieve the next channel page. |
| `sync_token` | query | `string` | no | Retrieve channels updated after the previous synced request. |
| `pinned` | query | `boolean` | no | When true, only pinned channels are returned. |
| `joined` | query | `boolean` | no | When true, only joined channels are returned. |
