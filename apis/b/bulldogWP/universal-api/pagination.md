# Bulldog-WP Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bulldog-WP expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bulldog-WP actions that support pagination

- [List campaign contacts](actions/get-campaign-contacts.md)
- [Get campaigns](actions/get-campaigns.md)
- [Search chat messages](actions/get-chat-messages.md)
- [Search chats](actions/get-device-chats.md)
- [List contacts](actions/get-device-contacts.md)
- [Search inbound files](actions/get-device-files.md)
- [Get numbers](actions/get-devices.md)
- [List labels](actions/get-labels.md)
- [Get users](actions/get-team-users.md)
- [List templates](actions/get-templates.md)
- [Get messaging prices](actions/get-waba-prices.md)
- [Get webhook logs](actions/get-webhook-logs.md)
- [Get webhooks](actions/get-webhooks.md)
- [Search files](actions/search-files.md)
- [Search messages](actions/search-messages.md)
