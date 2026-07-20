# Netlify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Netlify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Netlify actions that support pagination

- [List Form Submissions](actions/list-form-submissions.md)
- [List Site Builds](actions/list-site-builds.md)
- [List Site Deploys](actions/list-site-deploys.md)
- [List Site Submissions](actions/list-site-submissions.md)
- [List Sites](actions/list-sites.md)
