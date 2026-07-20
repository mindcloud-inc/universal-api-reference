# EMnify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model EMnify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-application-tokens?connectionId=$CONNECTION_ID&limit=25&offset=0&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## EMnify actions that support pagination

- [List Application Tokens](actions/list-application-tokens.md)
- [List Endpoint Events](actions/list-endpoint-events.md)
- [List Endpoints](actions/list-endpoints.md)
- [List Events](actions/list-events.md)
- [List SIMs](actions/list-sims.md)
