# <img src="https://images.mindcloud.co/apps/icons/c-dccontent-services_1777562763789.png" alt="CDC Content Services logo" width="28" height="28"> CDC Content Services: Universal API

Access CDC Content Services resources, including syndicated media, topics, tags, audiences, languages, organizations, and source metadata from the public CDC Content Services API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cDCContentServices/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tools.cdc.gov/api/docs/info.aspx
- **Vendor API docs:** https://tools.cdc.gov/api/docs/info.aspx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Media](actions/get-media.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from CDC Content Services. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from CDC Content Services. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | GET | Retrieves media from CDC Content Services by ID. |
| [List Media](actions/list-media.md) | GET | Retrieves media from CDC Content Services. |
| [List Media By Tag](actions/list-media-by-tag.md) | GET | Retrieves media by tag from CDC Content Services. |

### Media Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Content](actions/get-media-content.md) | GET | Retrieves media content from CDC Content Services. |

### Media Embed

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Embed Code](actions/get-media-embed-code.md) | GET | Retrieves media embed code from CDC Content Services. |

### Media Type

| Action | Method | Description |
| --- | --- | --- |
| [List Media Types](actions/list-media-types.md) | GET | Retrieves media types from CDC Content Services. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from CDC Content Services. |

### Organization Type

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Types](actions/list-organization-types.md) | GET | Retrieves organization types from CDC Content Services. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from CDC Content Services. |

### Syndicated Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Syndication](actions/get-media-syndication.md) | GET | Retrieves media syndication details from CDC Content Services. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from CDC Content Services. |
| [List Related Tags](actions/list-related-tags.md) | GET | Retrieves related tags from CDC Content Services. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from CDC Content Services. |

### Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [List Tag Types](actions/list-tag-types.md) | GET | Retrieves tag types from CDC Content Services. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [List Topics](actions/list-topics.md) | GET | Retrieves topics from CDC Content Services. |

