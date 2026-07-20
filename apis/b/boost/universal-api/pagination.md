# Boost Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Boost expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Boost actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Addresses](actions/list-addresses.md)
- [List AppFlows](actions/list-appflows.md)
- [List Automation Actions](actions/list-automation-actions.md)
- [List Automation Triggers](actions/list-automation-triggers.md)
- [List Business Cases](actions/list-business-cases.md)
- [List Business Contracts](actions/list-business-contracts.md)
- [List Business Offers](actions/list-business-offers.md)
- [List Business Orders](actions/list-business-orders.md)
- [List Charts](actions/list-charts.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Custom Modules](actions/list-custom-modules.md)
- [List Dashboards](actions/list-dashboards.md)
- [List Files](actions/list-files.md)
- [List Forms](actions/list-forms.md)
- [List Spaces](actions/list-spaces.md)
- [List Users](actions/list-users.md)
