# <img src="https://images.mindcloud.co/apps/icons/typeflo_1775747289979.png" alt="Typeflo logo" width="28" height="28"> Typeflo: Universal API

Manage Typeflo content and retrieve posts, pages, authors, categories, tags

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typeflo/latest
- **Category:** Website & App Building / CMS
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://typeflo.io
- **Vendor API docs:** https://typeflo.io/knowledge-base/category/headless-cms

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Authors](actions/list-authors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-authors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Get Author](actions/get-author.md) | GET | Retrieves an author profile from Typeflo. |
| [Get Author By Slug](actions/get-author-by-slug.md) | GET | Retrieves an author profile from Typeflo by slug. |
| [List Authors](actions/list-authors.md) | GET | Retrieves author profiles from the Typeflo site. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Typeflo. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from Typeflo. |
| [Get Category](actions/get-category.md) | GET | Retrieves a content category from Typeflo. |
| [Get Category By Slug](actions/get-category-by-slug.md) | GET | Retrieves a category from Typeflo by slug. |
| [List Categories](actions/list-categories.md) | GET | Retrieves content categories from the Typeflo site. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Typeflo. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a static page from Typeflo. |
| [Get Page By Slug](actions/get-page-by-slug.md) | GET | Retrieves a static page from Typeflo by slug. |
| [List Pages](actions/list-pages.md) | GET | Retrieves static site pages from Typeflo. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Typeflo. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from Typeflo. |
| [Get Post](actions/get-post.md) | GET | Retrieves a published post from Typeflo. |
| [Get Post By Slug](actions/get-post-by-slug.md) | GET | Retrieves a published post from Typeflo by slug. |
| [List Posts](actions/list-posts.md) | GET | Retrieves published blog posts from Typeflo. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in Typeflo. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Typeflo. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Typeflo. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a content tag from Typeflo. |
| [Get Tag By Slug](actions/get-tag-by-slug.md) | GET | Retrieves a tag from Typeflo by slug. |
| [List Tags](actions/list-tags.md) | GET | Retrieves content tags from the Typeflo site. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Typeflo. |

