# NewsBlur: Native API Reference

A consolidated summary of NewsBlur's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://newsblur.com/api
- **API base URL:** `https://www.newsblur.com`

## Authentication

### NewsBlur Login

Authenticate to NewsBlur with a username and password. NewsBlur returns session cookies from the login endpoint; subsequent API requests use those cookies.

### Credentials

- **Username:** `username` · required · NewsBlur username used with POST /api/login.
- **Password:** `password` · required · NewsBlur password used with POST /api/login.

[Official authentication documentation](https://newsblur.com/api)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Feed](actions/add-feed.md) | `POST /reader/add_url` | [docs](https://newsblur.com/api) |
| [Add Folder](actions/add-folder.md) | `POST /reader/add_folder` | [docs](https://newsblur.com/api) |
| [Autocomplete Feeds](actions/autocomplete-feeds.md) | `GET /rss_feeds/feed_autocomplete` | [docs](https://newsblur.com/api) |
| [Get Feed Page](actions/get-feed-page.md) | `GET /reader/page/:id` | [docs](https://newsblur.com/api) |
| [Get Feed Statistics](actions/get-feed-statistics.md) | `GET /rss_feeds/statistics/:id` | [docs](https://newsblur.com/api) |
| [Get Feed Stories](actions/get-feed-stories.md) | `GET /reader/feed/:id` | [docs](https://newsblur.com/api) |
| [Get Original Story](actions/get-original-story.md) | `GET /rss_feeds/original_story` | [docs](https://newsblur.com/api) |
| [Get Original Text](actions/get-original-text.md) | `GET /rss_feeds/original_text` | [docs](https://newsblur.com/api) |
| [Get River Stories](actions/get-river-stories.md) | `GET /reader/river_stories` | [docs](https://newsblur.com/api) |
| [Get Stories By Hash](actions/get-stories-by-hash.md) | `GET /reader/river_stories` | [docs](https://newsblur.com/api) |
| [List Favicons](actions/list-favicons.md) | `GET /reader/favicons` | [docs](https://newsblur.com/api) |
| [List Feed Trainers](actions/list-feed-trainers.md) | `GET /reader/feeds_trainer` | [docs](https://newsblur.com/api) |
| [List Feeds](actions/list-feeds.md) | `GET /reader/feeds` | [docs](https://newsblur.com/api) |
| [List Read Stories](actions/list-read-stories.md) | `GET /reader/read_stories` | [docs](https://newsblur.com/api) |
| [List Starred Stories](actions/list-starred-stories.md) | `GET /reader/starred_stories` | [docs](https://newsblur.com/api) |
| [List Starred Story Hashes](actions/list-starred-story-hashes.md) | `GET /reader/starred_story_hashes` | [docs](https://newsblur.com/api) |
| [List Unread Story Hashes](actions/list-unread-story-hashes.md) | `GET /reader/unread_story_hashes` | [docs](https://newsblur.com/api) |
| [Log In](actions/log-in.md) | `POST /api/login` | [docs](https://newsblur.com/api) |
| [Mark Feeds As Read](actions/mark-feeds-as-read.md) | `POST /reader/mark_feed_as_read` | [docs](https://newsblur.com/api) |
| [Mark Stories As Read](actions/mark-stories-as-read.md) | `POST /reader/mark_story_hashes_as_read` | [docs](https://newsblur.com/api) |
| [Mark Story As Unread](actions/mark-story-as-unread.md) | `POST /reader/mark_story_hash_as_unread` | [docs](https://newsblur.com/api) |
| [Refresh Feed Counts](actions/refresh-feed-counts.md) | `GET /reader/refresh_feeds` | [docs](https://newsblur.com/api) |
| [Save Story](actions/save-story.md) | `POST /reader/mark_story_hash_as_starred` | [docs](https://newsblur.com/api) |
| [Search Feed](actions/search-feed.md) | `GET /rss_feeds/search_feed` | [docs](https://newsblur.com/api) |
| [Unsave Story](actions/unsave-story.md) | `POST /reader/mark_story_hash_as_unstarred` | [docs](https://newsblur.com/api) |
