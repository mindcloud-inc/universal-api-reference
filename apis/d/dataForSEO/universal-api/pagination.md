# DataForSEO Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DataForSEO expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-competitor-domains?connectionId=$CONNECTION_ID&limit=25&offset=0&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DataForSEO actions that support pagination

- [Get Competitor Domains](actions/get-competitor-domains.md)
- [Get Domain Intersection](actions/get-domain-intersection.md)
- [Get Keyword Ideas](actions/get-keyword-ideas.md)
- [Get Keywords for Site](actions/get-keywords-for-site.md)
- [Get Page Intersection](actions/get-page-intersection.md)
- [Get Ranked Keywords](actions/get-ranked-keywords.md)
- [Get Relevant Pages](actions/get-relevant-pages.md)
- [Get Subdomains](actions/get-subdomains.md)
