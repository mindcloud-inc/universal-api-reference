# <img src="https://images.mindcloud.co/apps/icons/s-cotusblog_1776441813338.png" alt="SCOTUSblog logo" width="28" height="28"> SCOTUSblog: Universal API

Read Supreme Court news, analysis, and case coverage from SCOTUSblog

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sCOTUSblog/latest
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scotusblog.com/
- **Vendor API docs:** https://www.scotusblog.com/rss-feeds/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Abbe R. Gluck Posts](actions/list-abbe-r-gluck-posts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-abbe-r-gluck-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Abbe R. Gluck Posts](actions/list-abbe-r-gluck-posts.md) | GET |  |
| [List Adam Feldman Posts](actions/list-adam-feldman-posts.md) | GET |  |
| [List Akhil and Vikram Amar Posts](actions/list-akhil-and-vikram-amar-posts.md) | GET |  |
| [List Amy Howe Posts](actions/list-amy-howe-posts.md) | GET |  |
| [List Cases and Controversies Posts](actions/list-cases-and-controversies-posts.md) | GET |  |
| [List Cases in the Pipeline Posts](actions/list-cases-in-the-pipeline-posts.md) | GET |  |
| [List Class Actions Posts](actions/list-class-actions-posts.md) | GET |  |
| [List Court Analysis Posts](actions/list-court-analysis-posts.md) | GET |  |
| [List Court News Posts](actions/list-court-news-posts.md) | GET |  |
| [List Craig Konnoth Posts](actions/list-craig-konnoth-posts.md) | GET |  |
| [List Daniel Harawa Posts](actions/list-daniel-harawa-posts.md) | GET |  |
| [List Election Litigation Posts](actions/list-election-litigation-posts.md) | GET |  |
| [List Empirical SCOTUS Posts](actions/list-empirical-scotus-posts.md) | GET |  |
| [List Erwin Chemerinsky Posts](actions/list-erwin-chemerinsky-posts.md) | GET |  |
| [List Feed Items](actions/list-feed-items.md) | GET |  |
| [List Interim Docket Blog Posts](actions/list-interim-docket-blog-posts.md) | GET |  |
| [List John Elwood Posts](actions/list-john-elwood-posts.md) | GET |  |
| [List Kelsey Dallas and Nora Collins Posts](actions/list-kelsey-dallas-and-nora-collins-posts.md) | GET |  |
| [List Kelsey Dallas Posts](actions/list-kelsey-dallas-posts.md) | GET |  |
| [List Live Blog Posts](actions/list-live-blog-posts.md) | GET |  |
| [List Major Questions Posts](actions/list-major-questions-posts.md) | GET |  |
| [List Merits Cases Posts](actions/list-merits-cases-posts.md) | GET |  |
| [List Posts by Author](actions/list-posts-by-author.md) | GET |  |
| [List Posts by Category](actions/list-posts-by-category.md) | GET |  |
| [List Recurring Columns Posts](actions/list-recurring-columns-posts.md) | GET |  |
| [List Ronald Mann Posts](actions/list-ronald-mann-posts.md) | GET |  |
| [List Rory Little Posts](actions/list-rory-little-posts.md) | GET |  |
| [List Round-up Posts](actions/list-round-up-posts.md) | GET |  |
| [List SCOTUSblog Multi-author Posts](actions/list-scotusblog-multi-author-posts.md) | GET |  |
| [List Term in Review Posts](actions/list-term-in-review-posts.md) | GET |  |
| [List Uncategorized Posts](actions/list-uncategorized-posts.md) | GET |  |
| [List View from the Court Posts](actions/list-view-from-the-court-posts.md) | GET |  |
| [List What's Happening Now Posts](actions/list-whats-happening-now-posts.md) | GET |  |
| [List Zachary Shemtob Posts](actions/list-zachary-shemtob-posts.md) | GET |  |

