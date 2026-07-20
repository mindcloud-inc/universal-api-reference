# EasyBroker Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model EasyBroker expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## EasyBroker actions that support pagination

- [List Agencies](actions/list-agencies.md)
- [List Collaborations](actions/list-collaborations.md)
- [List Contact Requests](actions/list-contact-requests.md)
- [List Contacts](actions/list-contacts.md)
- [List MLS Properties](actions/list-mls-properties.md)
- [List Partner Contact Requests](actions/list-partner-contact-requests.md)
- [List Partner Property Listing Statuses](actions/list-partner-property-listing-statuses.md)
- [List Properties](actions/list-properties.md)
- [List Property Features](actions/list-property-features.md)
- [List Property Listing Statuses](actions/list-property-listing-statuses.md)
- [List Users](actions/list-users.md)
