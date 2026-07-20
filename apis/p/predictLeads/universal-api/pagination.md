# PredictLeads Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PredictLeads expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&location=United%20States&sizes=11-50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PredictLeads actions that support pagination

- [List Companies](actions/list-companies.md)
- [List Company Connections](actions/list-company-connections.md)
- [List Company Financing Events](actions/list-company-financing-events.md)
- [List Company GitHub Repositories](actions/list-company-git-hub-repositories.md)
- [List Company Job Openings](actions/list-company-job-openings.md)
- [List Company News Events](actions/list-company-news-events.md)
- [List Company Products](actions/list-company-products.md)
- [List Company Technologies](actions/list-company-technologies.md)
- [List Company Website Evolution](actions/list-company-website-evolution.md)
- [List Financing Events](actions/list-financing-events.md)
- [List Followed Companies](actions/list-followed-companies.md)
- [List Job Openings](actions/list-job-openings.md)
- [List News Events](actions/list-news-events.md)
- [List Portfolio Companies](actions/list-portfolio-companies.md)
- [List Products](actions/list-products.md)
- [List Startup Platform Posts](actions/list-startup-platform-posts.md)
- [List Technologies](actions/list-technologies.md)
- [List Technology Companies](actions/list-technology-companies.md)
