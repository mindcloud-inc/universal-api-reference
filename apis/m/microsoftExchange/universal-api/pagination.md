# Microsoft Exchange Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Microsoft Exchange expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-mailbox?connectionId=$CONNECTION_ID&limit=25&offset=0&userIdOrPrincipalName=user%40company.com%20or%20Entra%20user%20id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Microsoft Exchange actions that support pagination

- [List User Messages in Mailbox](actions/list-user-messages-in-mailbox.md)
