# <img src="https://images.mindcloud.co/apps/icons/lobstrs_1776184377708.png" alt="lobst.rs logo" width="28" height="28"> lobst.rs: Universal API

Track Lobsters stories, comments, users, tags, and links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lobstrs/latest
- **Category:** Marketing / Social Media
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lobste.rs
- **Vendor API docs:** https://lobste.rs/s/r9oskz/is_there_api_documentation_for_lobsters

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Stories by URL](actions/find-stories-by-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/find-stories-by-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fgithub.com%2Fjemalloc%2Fjemalloc%2Freleases%2Ftag%2F5.3.1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from lobst.rs. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Find Stories by URL](actions/find-stories-by-url.md) | GET | Finds stories in lobst.rs by URL. |
| [Get Story](actions/get-story.md) | GET | Retrieves a story from lobst.rs. |
| [Get Story by Slug](actions/get-story-by-slug.md) | GET | Retrieves a story from lobst.rs by slug. |
| [List Active Discussions](actions/list-active-discussions.md) | GET | Retrieves active discussions from lobst.rs. |
| [List Hottest Stories](actions/list-hottest-stories.md) | GET | Retrieves hottest stories from lobst.rs. |
| [List Newest Stories](actions/list-newest-stories.md) | GET | Retrieves newest stories from lobst.rs. |
| [List Stories by Category](actions/list-stories-by-category.md) | GET | Finds stories in lobst.rs by category. |
| [List Stories by Domain](actions/list-stories-by-domain.md) | GET | Finds stories in lobst.rs by domain. |
| [List Stories by Tag](actions/list-stories-by-tag.md) | GET | Finds stories in lobst.rs by tag. |
| [List User Stories](actions/list-user-stories.md) | GET | Retrieves stories from lobst.rs by user. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from lobst.rs. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves a user profile from lobst.rs. |

