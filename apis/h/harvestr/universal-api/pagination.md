# Harvestr.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Harvestr.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Harvestr.io actions that support pagination

- [List Companies](actions/list-companies.md)
- [List Company Attribute Values](actions/list-company-attribute-values.md)
- [List Company Attributes](actions/list-company-attributes.md)
- [List Components](actions/list-components.md)
- [List Custom Inboxes](actions/list-custom-inboxes.md)
- [List Discoveries](actions/list-discoveries.md)
- [List Discovery Feedback](actions/list-discovery-feedback.md)
- [List Discovery States](actions/list-discovery-states.md)
- [List Feedback](actions/list-feedback.md)
- [List Message Feedback](actions/list-message-feedback.md)
- [List Messages](actions/list-messages.md)
- [List User Attribute Values](actions/list-user-attribute-values.md)
- [List User Attributes](actions/list-user-attributes.md)
- [List Users](actions/list-users.md)
