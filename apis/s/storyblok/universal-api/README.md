# <img src="https://images.mindcloud.co/apps/icons/storyblok-icon_1775828596982.png" alt="Storyblok logo" width="28" height="28"> Storyblok: Universal API

Read Storyblok content, links, tags, datasources, and assets from the Content Delivery API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/storyblok/latest
- **Category:** Website & App Building / CMS
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.storyblok.com
- **Vendor API docs:** https://www.storyblok.com/docs/api/content-delivery/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Space](actions/get-current-space.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-current-space?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Signed Asset URL](actions/get-signed-asset-url.md) | GET | Retrieves a signed URL for a private Storyblok asset. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Get Datasource](actions/get-datasource.md) | GET | Retrieves a Storyblok datasource by slug. |
| [List Datasource Entries](actions/list-datasource-entries.md) | GET | Retrieves datasource entries from Storyblok by datasource. |
| [List Datasources](actions/list-datasources.md) | GET | Retrieves datasources from the current Storyblok space. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Links in Folder](actions/list-links-in-folder.md) | GET | Retrieves Storyblok links from a specific folder. |
| [List Stories in Folder](actions/list-stories-in-folder.md) | GET | Retrieves stories from a specific Storyblok folder. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Filter Stories](actions/filter-stories.md) | GET | Retrieves Storyblok stories using a filter query. |
| [Get Link by UUID](actions/get-link-by-path.md) | GET | Retrieves a Storyblok link by UUID. |
| [Get Story by Slug](actions/get-story-by-slug.md) | GET | Retrieves a Storyblok story by slug. |
| [Get Story by UUID](actions/get-story-by-uuid.md) | GET | Retrieves a Storyblok story by UUID. |
| [Get Story from Release](actions/get-story-from-release.md) | GET | Retrieves a Storyblok story from a specific release. |
| [List Links](actions/list-links.md) | GET | Retrieves Storyblok links for the current space. |
| [List Stories](actions/list-stories.md) | GET | Retrieves stories from Storyblok for the current space. |
| [List Stories by Content Type](actions/list-stories-by-content-type.md) | GET | Retrieves Storyblok stories for a specific content type. |
| [List Stories by Language](actions/list-stories-by-language.md) | GET | Retrieves Storyblok stories in a specific language. |
| [List Stories by UUIDs](actions/list-stories-by-uui-ds.md) | GET | Retrieves Storyblok stories for specific UUIDs. |
| [List Stories in Workflow Stage](actions/list-stories-in-workflow-stage.md) | GET | Retrieves Storyblok stories in specific workflow stages. |
| [List Stories with Resolved Relations](actions/list-stories-with-resolved-relations.md) | GET | Retrieves Storyblok stories with resolved relations. |
| [Search Stories](actions/search-stories.md) | GET | Finds Storyblok stories by search term. |
| [Sort Stories](actions/sort-stories.md) | GET | Retrieves Storyblok stories sorted by story properties. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Stories by Tag](actions/list-stories-by-tag.md) | GET | Retrieves Storyblok stories with a specific tag. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags used in the current Storyblok space. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Space](actions/get-current-space.md) | GET | Retrieves the current space from Storyblok. |

