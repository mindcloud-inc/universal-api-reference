# <img src="https://images.mindcloud.co/apps/icons/contentful_1773946469831.png" alt="Contentful logo" width="28" height="28"> Contentful: Universal API

Manage content, entries, assets, and environments in Contentful

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contentful/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.contentful.com/
- **Vendor API docs:** https://www.contentful.com/developers/docs/references/content-management-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List spaces](actions/list-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Archive asset](actions/archive-asset.md) | PUT |  |
| [Create asset](actions/create-asset.md) | POST |  |
| [Create or update asset](actions/create-or-update-asset.md) | PUT |  |
| [Delete asset](actions/delete-asset.md) | DELETE |  |
| [Get asset](actions/get-asset.md) | GET |  |
| [List assets](actions/list-assets.md) | GET |  |
| [Process asset](actions/process-asset.md) | PUT |  |
| [Publish asset](actions/publish-asset.md) | PUT |  |
| [Unarchive asset](actions/unarchive-asset.md) | PUT |  |
| [Unpublish asset](actions/unpublish-asset.md) | PUT |  |

### Content Type

| Action | Method | Description |
| --- | --- | --- |
| [Activate content type](actions/activate-content-type.md) | PUT |  |
| [Create content type](actions/create-content-type.md) | POST |  |
| [Create content type with ID](actions/create-content-type-with-id.md) | POST |  |
| [Deactivate content type](actions/deactivate-content-type.md) | PUT |  |
| [Delete content type](actions/delete-content-type.md) | DELETE |  |
| [Get content type](actions/get-content-type.md) | GET |  |
| [List content types](actions/list-content-types.md) | GET |  |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Archive entry](actions/archive-entry.md) | PUT |  |
| [Create entry](actions/create-entry.md) | POST |  |
| [Create entry with ID](actions/create-entry-with-id.md) | POST |  |
| [Delete entry](actions/delete-entry.md) | DELETE |  |
| [Get entry](actions/get-entry.md) | GET |  |
| [List entries](actions/list-entries.md) | GET |  |
| [Patch entry](actions/patch-entry.md) | PUT |  |
| [Publish entry](actions/publish-entry.md) | PUT |  |
| [Unarchive entry](actions/unarchive-entry.md) | PUT |  |
| [Unpublish entry](actions/unpublish-entry.md) | PUT |  |
| [Update entry](actions/update-entry.md) | PUT |  |

### Entry Reference

| Action | Method | Description |
| --- | --- | --- |
| [Get entry references](actions/get-entry-references.md) | GET |  |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get environment](actions/get-environment.md) | GET |  |
| [List environments](actions/list-environments.md) | GET |  |

### Environment Alias

| Action | Method | Description |
| --- | --- | --- |
| [Get environment alias](actions/get-environment-alias.md) | GET |  |
| [List environment aliases](actions/list-environment-aliases.md) | GET |  |

### Locale

| Action | Method | Description |
| --- | --- | --- |
| [Create locale](actions/create-locale.md) | POST |  |
| [Delete locale](actions/delete-locale.md) | DELETE |  |
| [Get locale](actions/get-locale.md) | GET |  |
| [List locales](actions/list-locales.md) | GET |  |
| [Update locale](actions/update-locale.md) | PUT |  |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Get space](actions/get-space.md) | GET |  |
| [List spaces](actions/list-spaces.md) | GET |  |

