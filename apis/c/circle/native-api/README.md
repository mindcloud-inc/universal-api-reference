# Circle: Native API Reference

A consolidated summary of Circle's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.circle.so/apis/admin-api
- **OpenAPI specification:** https://api-headless.circle.so/api/admin/v2/swagger.yaml
- **API base URL:** `https://{subdomain}.circle.so`

## Authentication

### API Token

Circle Admin API token auth. Use the API access token as the credential and send Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · Circle host value required by Admin API requests

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-headless.circle.so/admin-api-v2-quick-start)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Space Member](actions/add-space-member.md) | `POST /api/admin/v2/space_members` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Access Group](actions/create-access-group.md) | `POST /api/admin/v2/access_groups` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Basic Post](actions/create-basic-post.md) | `POST /api/admin/v2/posts` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Comment](actions/create-comment.md) | `POST /api/admin/v2/comments` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Community Member](actions/create-community-member.md) | `POST /api/admin/v2/community_members` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Community Segment](actions/create-community-segment.md) | `POST /api/admin/v2/community_segments` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Event](actions/create-event.md) | `POST /api/admin/v2/events` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Member Tag](actions/create-member-tag.md) | `POST /api/admin/v2/member_tags` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Space](actions/create-space.md) | `POST /api/admin/v2/spaces` | [docs](https://api.circle.so/apis/admin-api) |
| [Create Topic](actions/create-topic.md) | `POST /api/admin/v2/topics` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Basic Post](actions/get-basic-post.md) | `GET /api/admin/v2/posts/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Comment](actions/get-comment.md) | `GET /api/admin/v2/comments/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Community](actions/get-community.md) | `GET /api/admin/v2/community` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Community Member](actions/get-community-member.md) | `GET /api/admin/v2/community_members/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Event](actions/get-event.md) | `GET /api/admin/v2/events/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Member Tag](actions/get-member-tag.md) | `GET /api/admin/v2/member_tags/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Space](actions/get-space.md) | `GET /api/admin/v2/spaces/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Get Topic](actions/get-topic.md) | `GET /api/admin/v2/topics/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [List Access Groups](actions/list-access-groups.md) | `GET /api/admin/v2/access_groups` | [docs](https://api.circle.so/apis/admin-api) |
| [List Basic Posts](actions/list-basic-posts.md) | `GET /api/admin/v2/posts` | [docs](https://api.circle.so/apis/admin-api) |
| [List Comments](actions/list-comments.md) | `GET /api/admin/v2/comments` | [docs](https://api.circle.so/apis/admin-api) |
| [List Community Member Spaces](actions/list-community-member-spaces.md) | `GET /api/admin/v2/community_member_spaces` | [docs](https://api.circle.so/apis/admin-api) |
| [List Community Members](actions/list-community-members.md) | `GET /api/admin/v2/community_members` | [docs](https://api.circle.so/apis/admin-api) |
| [List Community Segments](actions/list-community-segments.md) | `GET /api/admin/v2/community_segments` | [docs](https://api.circle.so/apis/admin-api) |
| [List Events](actions/list-events.md) | `GET /api/admin/v2/events` | [docs](https://api.circle.so/apis/admin-api) |
| [List Member Tags](actions/list-member-tags.md) | `GET /api/admin/v2/member_tags` | [docs](https://api.circle.so/apis/admin-api) |
| [List Profile Fields](actions/list-profile-fields.md) | `GET /api/admin/v2/profile_fields` | [docs](https://api.circle.so/apis/admin-api) |
| [List Space Members](actions/list-space-members.md) | `GET /api/admin/v2/space_members` | [docs](https://api.circle.so/apis/admin-api) |
| [List Spaces](actions/list-spaces.md) | `GET /api/admin/v2/spaces` | [docs](https://api.circle.so/apis/admin-api) |
| [List Topics](actions/list-topics.md) | `GET /api/admin/v2/topics` | [docs](https://api.circle.so/apis/admin-api) |
| [Search Community Members](actions/search-community-members.md) | `GET /api/admin/v2/community_members/search` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Access Group](actions/update-access-group.md) | `PUT /api/admin/v2/access_groups/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Basic Post](actions/update-basic-post.md) | `PUT /api/admin/v2/posts/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Community](actions/update-community.md) | `PUT /api/admin/v2/community` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Community Member](actions/update-community-member.md) | `PUT /api/admin/v2/community_members/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Community Segment](actions/update-community-segment.md) | `PUT /api/admin/v2/community_segments/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Event](actions/update-event.md) | `PUT /api/admin/v2/events/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Member Tag](actions/update-member-tag.md) | `PUT /api/admin/v2/member_tags/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Space](actions/update-space.md) | `PUT /api/admin/v2/spaces/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
| [Update Topic](actions/update-topic.md) | `PUT /api/admin/v2/topics/[:id]` | [docs](https://api.circle.so/apis/admin-api) |
