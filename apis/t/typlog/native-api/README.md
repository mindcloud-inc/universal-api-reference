# Typlog: Native API Reference

A consolidated summary of Typlog's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.typlog.com/
- **OpenAPI specification:** https://api.typlog.com/openapi.yml
- **API base URL:** `https://api.typlog.com/v3`

## Authentication

### API Key

Use a Typlog personal API token. MindCloud will use the platform-managed apiKey credential contract for authenticated requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://typlog.com/changelog/v3-0)

## API conventions

The next-page cursor is read from `next`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Episode](actions/create-episode.md) | `POST /episodes` | [docs](https://api.typlog.com/) |
| [Create Page](actions/create-page.md) | `POST /pages` | [docs](https://api.typlog.com/) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://api.typlog.com/) |
| [Get Author](actions/get-author.md) | `GET /authors/[:id]` | [docs](https://api.typlog.com/) |
| [Get Episode](actions/get-episode.md) | `GET /episodes/[:id]` | [docs](https://api.typlog.com/) |
| [Get Page](actions/get-page.md) | `GET /pages/[:id]` | [docs](https://api.typlog.com/) |
| [Get Post](actions/get-post.md) | `GET /posts/[:id]` | [docs](https://api.typlog.com/) |
| [Get Site](actions/get-site.md) | `GET /sites/[:id]` | [docs](https://api.typlog.com/) |
| [Get Tag](actions/get-tag.md) | `GET /tags/[:id]` | [docs](https://api.typlog.com/) |
| [List Authors](actions/list-authors.md) | `GET /authors` | [docs](https://api.typlog.com/) |
| [List Episodes](actions/list-episodes.md) | `GET /episodes` | [docs](https://api.typlog.com/) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://api.typlog.com/) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://api.typlog.com/) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://api.typlog.com/) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://api.typlog.com/) |
| [Save Episode Content](actions/save-episode-content.md) | `POST /episodes/[:id]/content` | [docs](https://api.typlog.com/) |
| [Save Page Content](actions/save-page-content.md) | `POST /pages/[:id]/content` | [docs](https://api.typlog.com/) |
| [Save Post Content](actions/save-post-content.md) | `POST /posts/[:id]/content` | [docs](https://api.typlog.com/) |
| [Set Episode Status](actions/set-episode-status.md) | `POST /episodes/[:id]/status` | [docs](https://api.typlog.com/) |
| [Set Page Status](actions/set-page-status.md) | `POST /pages/[:id]/status` | [docs](https://api.typlog.com/) |
| [Set Post Status](actions/set-post-status.md) | `POST /posts/[:id]/status` | [docs](https://api.typlog.com/) |
| [Update Episode](actions/update-episode.md) | `PUT /episodes/[:id]` | [docs](https://api.typlog.com/) |
| [Update Page](actions/update-page.md) | `PUT /pages/[:id]` | [docs](https://api.typlog.com/) |
| [Update Post](actions/update-post.md) | `PUT /posts/[:id]` | [docs](https://api.typlog.com/) |
