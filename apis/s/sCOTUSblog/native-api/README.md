# SCOTUSblog: Native API Reference

A consolidated summary of SCOTUSblog's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://www.scotusblog.com/rss-feeds/
- **API base URL:** `https://www.scotusblog.com`

## Authentication

### No Authentication

SCOTUSblog's public RSS feeds do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://www.scotusblog.com/rss-feeds/)

## API conventions

Responses from this API use XML.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Abbe R. Gluck Posts](actions/list-abbe-r-gluck-posts.md) | `GET /author/abbe-gluck/feed/` | [docs](https://www.scotusblog.com/author/abbe-gluck/) |
| [List Adam Feldman Posts](actions/list-adam-feldman-posts.md) | `GET /author/adam-feldman/feed/` | [docs](https://www.scotusblog.com/author/adam-feldman/) |
| [List Akhil and Vikram Amar Posts](actions/list-akhil-and-vikram-amar-posts.md) | `GET /author/amar/feed/` | [docs](https://www.scotusblog.com/author/amar/) |
| [List Amy Howe Posts](actions/list-amy-howe-posts.md) | `GET /author/amy-howe/feed/` | [docs](https://www.scotusblog.com/author/amy-howe/) |
| [List Cases and Controversies Posts](actions/list-cases-and-controversies-posts.md) | `GET /category/cases-and-controversies/feed/` | [docs](https://www.scotusblog.com/category/cases-and-controversies/) |
| [List Cases in the Pipeline Posts](actions/list-cases-in-the-pipeline-posts.md) | `GET /category/cases-in-the-pipeline/feed/` | [docs](https://www.scotusblog.com/category/cases-in-the-pipeline/) |
| [List Class Actions Posts](actions/list-class-actions-posts.md) | `GET /category/class-actions/feed/` | [docs](https://www.scotusblog.com/category/class-actions/) |
| [List Court Analysis Posts](actions/list-court-analysis-posts.md) | `GET /category/court-analysis/feed/` | [docs](https://www.scotusblog.com/category/court-analysis/) |
| [List Court News Posts](actions/list-court-news-posts.md) | `GET /category/court-news/feed/` | [docs](https://www.scotusblog.com/category/court-news/) |
| [List Craig Konnoth Posts](actions/list-craig-konnoth-posts.md) | `GET /author/ckonnoth/feed/` | [docs](https://www.scotusblog.com/author/ckonnoth/) |
| [List Daniel Harawa Posts](actions/list-daniel-harawa-posts.md) | `GET /author/daniel-harawa/feed/` | [docs](https://www.scotusblog.com/author/daniel-harawa/) |
| [List Election Litigation Posts](actions/list-election-litigation-posts.md) | `GET /category/election-litigation/feed/` | [docs](https://www.scotusblog.com/category/election-litigation/) |
| [List Empirical SCOTUS Posts](actions/list-empirical-scotus-posts.md) | `GET /category/empirical-scotus/feed/` | [docs](https://www.scotusblog.com/category/archive/empirical-scotus/) |
| [List Erwin Chemerinsky Posts](actions/list-erwin-chemerinsky-posts.md) | `GET /author/erwin-chemerinsky/feed/` | [docs](https://www.scotusblog.com/author/erwin-chemerinsky/) |
| [List Feed Items](actions/list-feed-items.md) | `GET /feed/` | [docs](https://www.scotusblog.com/rss-feeds/) |
| [List Interim Docket Blog Posts](actions/list-interim-docket-blog-posts.md) | `GET /category/interim-docket-blog/feed/` | [docs](https://www.scotusblog.com/category/interim-docket-blog/) |
| [List John Elwood Posts](actions/list-john-elwood-posts.md) | `GET /author/john-elwood/feed/` | [docs](https://www.scotusblog.com/author/john-elwood/) |
| [List Kelsey Dallas and Nora Collins Posts](actions/list-kelsey-dallas-and-nora-collins-posts.md) | `GET /author/kelsey-dallas-and-nora-collins/feed/` | [docs](https://www.scotusblog.com/author/kelsey-dallas-and-nora-collins/) |
| [List Kelsey Dallas Posts](actions/list-kelsey-dallas-posts.md) | `GET /author/kelseythedispatch-com/feed/` | [docs](https://www.scotusblog.com/author/kelseythedispatch-com/) |
| [List Live Blog Posts](actions/list-live-blog-posts.md) | `GET /category/live/feed/` | [docs](https://www.scotusblog.com/category/live/) |
| [List Major Questions Posts](actions/list-major-questions-posts.md) | `GET /category/major-questions/feed/` | [docs](https://www.scotusblog.com/category/major-questions/) |
| [List Merits Cases Posts](actions/list-merits-cases-posts.md) | `GET /category/merits-cases/feed/` | [docs](https://www.scotusblog.com/category/merits-cases/) |
| [List Posts by Author](actions/list-posts-by-author.md) | `GET /author/:authorSlug/feed/` | [docs](https://www.scotusblog.com/2010/11/scotusblog-4-0-and-the-rss-feeds-feature/) |
| [List Posts by Category](actions/list-posts-by-category.md) | `GET /category/:categorySlug/feed/` | [docs](https://www.scotusblog.com/2010/11/scotusblog-4-0-and-the-rss-feeds-feature/) |
| [List Recurring Columns Posts](actions/list-recurring-columns-posts.md) | `GET /category/recurring-columns/feed/` | [docs](https://www.scotusblog.com/category/recurring-columns/) |
| [List Ronald Mann Posts](actions/list-ronald-mann-posts.md) | `GET /author/ronald-mann/feed/` | [docs](https://www.scotusblog.com/author/ronald-mann/) |
| [List Rory Little Posts](actions/list-rory-little-posts.md) | `GET /author/rory-little/feed/` | [docs](https://www.scotusblog.com/author/rory-little/) |
| [List Round-up Posts](actions/list-round-up-posts.md) | `GET /category/round-up/feed/` | [docs](https://www.scotusblog.com/category/round-up/) |
| [List SCOTUSblog Multi-author Posts](actions/list-scotusblog-multi-author-posts.md) | `GET /author/edith-roberts-amy-howe-kalvis-golde-and-katie-bart/feed/` | [docs](https://www.scotusblog.com/author/edith-roberts-amy-howe-kalvis-golde-and-katie-bart/) |
| [List Term in Review Posts](actions/list-term-in-review-posts.md) | `GET /category/term-in-review/feed/` | [docs](https://www.scotusblog.com/category/term-in-review/) |
| [List Uncategorized Posts](actions/list-uncategorized-posts.md) | `GET /category/uncategorized/feed/` | [docs](https://www.scotusblog.com/category/uncategorized/) |
| [List View from the Court Posts](actions/list-view-from-the-court-posts.md) | `GET /category/view-from-the-court/feed/` | [docs](https://www.scotusblog.com/category/view-from-the-court/) |
| [List What's Happening Now Posts](actions/list-whats-happening-now-posts.md) | `GET /category/whats-happening-now/feed/` | [docs](https://www.scotusblog.com/category/whats-happening-now/) |
| [List Zachary Shemtob Posts](actions/list-zachary-shemtob-posts.md) | `GET /author/zachary/feed/` | [docs](https://www.scotusblog.com/author/zachary/) |
