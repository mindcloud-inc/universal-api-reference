# <img src="https://images.mindcloud.co/apps/icons/favicon-3_1773336522390.png" alt="Ghost logo" width="28" height="28"> Ghost: Universal API

Create, publish, and manage Ghost posts, members, and newsletters

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ghost/latest
- **Category:** Website & App Building / CMS
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ghost.org
- **Vendor API docs:** https://docs.ghost.org/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Posts](actions/list-posts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Upload Image](actions/upload-image.md) | POST | Uploads an image to Ghost. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a new member in Ghost. |
| [List Members](actions/list-members.md) | GET | Retrieves members from Ghost. |
| [Update Member](actions/update-member.md) | PUT | Updates an existing member in Ghost. |

### Newsletter

| Action | Method | Description |
| --- | --- | --- |
| [Create Newsletter](actions/create-newsletter.md) | POST | Creates a new newsletter in Ghost. |
| [List Newsletters](actions/list-newsletters.md) | GET | Retrieves newsletters from Ghost. |
| [Update Newsletter](actions/update-newsletter.md) | PUT | Updates an existing newsletter in Ghost. |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Create Offer](actions/create-offer.md) | POST | Creates a new offer in Ghost. |
| [List Offers](actions/list-offers.md) | GET | Retrieves offers from Ghost. |
| [Update Offer](actions/update-offer.md) | PUT | Updates an existing offer in Ghost. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Copy Page](actions/copy-page.md) | POST | Creates a copy of a page in Ghost. |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Ghost. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Ghost. |
| [Get Page by ID](actions/get-page-by-id.md) | GET | Retrieves a page from Ghost by ID. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Ghost. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Ghost. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Ghost. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from Ghost. |
| [Get Post by ID](actions/get-post-by-id.md) | GET | Retrieves a post from Ghost by ID. |
| [Get Post by Slug](actions/get-post-by-slug.md) | GET | Retrieves a post from Ghost by slug. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Ghost. |
| [Publish Post](actions/publish-post.md) | PUT | Publishes a draft post in Ghost. |
| [Schedule Post](actions/schedule-post.md) | PUT | Schedules a post in Ghost. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in Ghost. |

### Tier

| Action | Method | Description |
| --- | --- | --- |
| [Create Tier](actions/create-tier.md) | POST | Creates a new tier in Ghost. |
| [List Tiers](actions/list-tiers.md) | GET | Retrieves tiers from Ghost. |
| [Update Tier](actions/update-tier.md) | PUT | Updates an existing tier in Ghost. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Ghost. |

