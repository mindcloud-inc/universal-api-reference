# Planning Center Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Planning Center expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-campuses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Planning Center actions that support pagination

- [List Campuses](actions/list-campuses.md)
- [List Household People](actions/list-household-people.md)
- [List Households](actions/list-households.md)
- [List List Results](actions/list-list-results.md)
- [List Lists](actions/list-lists.md)
- [List People](actions/list-people.md)
- [List Person Addresses](actions/list-person-addresses.md)
- [List Person Emails](actions/list-person-emails.md)
- [List Person Field Data](actions/list-person-field-data.md)
- [List Person Households](actions/list-person-households.md)
- [List Person Notes](actions/list-person-notes.md)
- [List Person Phone Numbers](actions/list-person-phone-numbers.md)
- [List Workflow Cards](actions/list-workflow-cards.md)
- [List Workflows](actions/list-workflows.md)
