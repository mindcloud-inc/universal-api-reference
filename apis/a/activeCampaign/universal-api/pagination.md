# ActiveCampaign Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ActiveCampaign expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ActiveCampaign actions that support pagination

- [List Accounts](actions/list-accounts.md)
- [List Automations](actions/list-automations.md)
- [List Contact Automations](actions/list-contact-automations.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Field Values](actions/list-custom-field-values.md)
- [List Deal Stages](actions/list-deal-stages.md)
- [List Deals](actions/list-deals.md)
- [List Lists](actions/list-lists.md)
- [List Pipelines](actions/list-pipelines.md)
