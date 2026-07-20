# e-Boekhouden.nl Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model e-Boekhouden.nl expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-administrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## e-Boekhouden.nl actions that support pagination

- [List Administrations](actions/list-administrations.md)
- [List Cost Centers](actions/list-cost-centers.md)
- [List Email Templates](actions/list-email-templates.md)
- [List Invoice Templates](actions/list-invoice-templates.md)
- [List Invoices](actions/list-invoices.md)
- [List Ledgers](actions/list-ledgers.md)
- [List Linked Administrations](actions/list-linked-administrations.md)
- [List Members](actions/list-members.md)
- [List Mutations](actions/list-mutations.md)
- [List Outstanding Invoices](actions/list-outstanding-invoices.md)
- [List Products](actions/list-products.md)
- [List Relations](actions/list-relations.md)
- [List Units](actions/list-units.md)
