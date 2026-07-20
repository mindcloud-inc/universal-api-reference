# <img src="https://images.mindcloud.co/apps/icons/centers-for-disease-control-and-prevention_1776359311904.png" alt="Centers for Disease Control and Prevention logo" width="28" height="28"> Centers for Disease Control and Prevention: Universal API

Search and retrieve CDC public health content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/centersForDiseaseControlAndPrevention/latest
- **Category:** Website & App Building / CMS
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cdc.gov
- **Vendor API docs:** https://tools.cdc.gov/api/docs/info.aspx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Media](actions/get-media.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from CDC Content Services. |
| [List Topics](actions/list-topics.md) | GET | Retrieves topics from CDC Content Services. |

### Creative Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | GET | Retrieves media from CDC Content Services by ID. |
| [Get Media Content](actions/get-media-content.md) | GET | Retrieves media content from CDC Content Services. |
| [Get Media Embed Code](actions/get-media-embed-code.md) | GET | Retrieves media embed code from CDC Content Services. |
| [Get Media Syndicated HTML](actions/get-media-syndicated-html.md) | GET | Retrieves syndicated HTML for media from CDC Content Services. |
| [List Media By Tag](actions/list-media-by-tag.md) | GET | Retrieves media by tag from CDC Content Services. |
| [List Media Types](actions/list-media-types.md) | GET | Retrieves media types from CDC Content Services. |
| [Search Media](actions/search-media.md) | GET | Finds media in CDC Content Services. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Types](actions/list-organization-types.md) | GET | Retrieves organization types from CDC Content Services. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from CDC Content Services. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from CDC Content Services. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from CDC Content Services. |
| [List Related Tags](actions/list-related-tags.md) | GET | Retrieves related tags from CDC Content Services. |
| [List Tag Types](actions/list-tag-types.md) | GET | Retrieves tag types from CDC Content Services. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from CDC Content Services. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from CDC Content Services. |

