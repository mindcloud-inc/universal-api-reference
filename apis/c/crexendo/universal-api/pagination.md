# Crexendo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Crexendo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-call-queues?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Crexendo actions that support pagination

- [List Call Queues](actions/list-call-queues.md)
- [List Domain Active Calls](actions/list-domain-active-calls.md)
- [List Domain Addresses](actions/list-domain-addresses.md)
- [List Domain Agents](actions/list-domain-agents.md)
- [List Domain Contacts](actions/list-domain-contacts.md)
- [List Domain Phone Numbers](actions/list-domain-phone-numbers.md)
- [List Domain SMS Numbers](actions/list-domain-sms-numbers.md)
- [List Domains](actions/list-domains.md)
- [List My Answer Rules](actions/list-my-answer-rules.md)
- [List My Contacts](actions/list-my-contacts.md)
- [List Phone Numbers](actions/list-phone-numbers.md)
- [List Sites](actions/list-sites.md)
- [List User Active Calls](actions/list-user-active-calls.md)
- [List User Addresses](actions/list-user-addresses.md)
- [List User Contacts](actions/list-user-contacts.md)
- [List User Devices](actions/list-user-devices.md)
- [List User Meetings](actions/list-user-meetings.md)
- [List User SMS Numbers](actions/list-user-sms-numbers.md)
- [List Users](actions/list-users.md)
