# Paradym Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Paradym expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-certificates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Paradym actions that support pagination

- [List Certificates](actions/list-certificates.md)
- [List DIDs](actions/list-dids.md)
- [List Issued Credentials](actions/list-issued-credentials.md)
- [List Mdoc Credential Templates](actions/list-mdoc-credential-templates.md)
- [List Presentation Templates](actions/list-presentation-templates.md)
- [List Project Members](actions/list-project-members.md)
- [List Projects](actions/list-projects.md)
- [List Sd-Jwt Vc Credential Templates](actions/list-sd-jwt-vc-credential-templates.md)
- [List Trusted Entities](actions/list-trusted-entities.md)
- [List Webhooks](actions/list-webhooks.md)
