# <img src="https://images.mindcloud.co/apps/icons/kontentai_1776884920748.png" alt="Kontent.ai logo" width="28" height="28"> Kontent.ai: Universal API

Manage and retrieve Kontent.ai content, assets, collections, languages, taxonomies, content type snippets, custom apps, and Delivery API resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kontentai/latest
- **Category:** Website & App Building / CMS
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kontent.ai/
- **Vendor API docs:** https://kontent.ai/learn/docs/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List management languages](actions/list-management-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-management-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List custom apps](actions/list-custom-apps.md) | GET | Retrieves custom apps from your Kontent.ai environment. |
| [Retrieve custom app](actions/retrieve-custom-app.md) | GET | Retrieves a custom app from Kontent.ai. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Add management asset](actions/add-management-asset.md) | POST | Creates a new asset in Kontent.ai. |
| [Delete management asset](actions/delete-management-asset.md) | DELETE | Deletes an asset from your Kontent.ai environment. |
| [List management assets](actions/list-management-assets.md) | GET | Retrieves assets from your Kontent.ai environment. |
| [Retrieve management asset](actions/retrieve-management-asset.md) | GET | Retrieves an asset from your Kontent.ai environment. |
| [Upsert management asset](actions/upsert-management-asset.md) | PUT | Upserts an asset in Kontent.ai by external ID. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Add management taxonomy group](actions/add-management-taxonomy-group.md) | POST | Creates a new taxonomy group in Kontent.ai. |
| [Delete management taxonomy group](actions/delete-management-taxonomy-group.md) | DELETE | Deletes a taxonomy group from Kontent.ai. |
| [List management taxonomy groups](actions/list-management-taxonomy-groups.md) | GET | Retrieves taxonomy groups from your Kontent.ai environment. |
| [Modify management taxonomy group](actions/modify-management-taxonomy-group.md) | PUT | Modifies a taxonomy group in Kontent.ai. |
| [Retrieve management taxonomy group](actions/retrieve-management-taxonomy-group.md) | GET | Retrieves a taxonomy group from Kontent.ai. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List management collections](actions/list-management-collections.md) | GET | Retrieves collections from your Kontent.ai environment. |
| [Modify management collections](actions/modify-management-collections.md) | PUT | Modifies collections in your Kontent.ai environment. |

### Content Item

| Action | Method | Description |
| --- | --- | --- |
| [Enumerate content items](actions/enumerate-content-items.md) | GET | Enumerates all content items from Kontent.ai. |
| [List content items](actions/list-content-items.md) | GET | Retrieves content items from your Kontent.ai environment. |
| [List items referencing asset](actions/list-items-referencing-asset.md) | GET | Retrieves items referencing an asset in Kontent.ai. |
| [List items referencing item](actions/list-items-referencing-item.md) | GET | Retrieves items referencing a content item in Kontent.ai. |
| [Retrieve content item](actions/retrieve-content-item.md) | GET | Retrieves a content item from Kontent.ai by codename. |

### Content Type

| Action | Method | Description |
| --- | --- | --- |
| [List content types](actions/list-content-types.md) | GET | Retrieves content types from your Kontent.ai environment. |
| [Retrieve content type](actions/retrieve-content-type.md) | GET | Retrieves a content type from Kontent.ai. |

### Content Type Element

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve content type element](actions/retrieve-content-type-element.md) | GET | Retrieves a content type element from Kontent.ai. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add content type snippet](actions/add-content-type-snippet.md) | POST | Creates a new content type snippet in Kontent.ai. |
| [Delete content type snippet](actions/delete-content-type-snippet.md) | DELETE | Deletes a content type snippet from Kontent.ai. |
| [List content type snippets](actions/list-content-type-snippets.md) | GET | Retrieves content type snippets from Kontent.ai. |
| [Modify content type snippet](actions/modify-content-type-snippet.md) | PUT | Modifies a content type snippet in Kontent.ai. |
| [Retrieve content type snippet](actions/retrieve-content-type-snippet.md) | GET | Retrieves a content type snippet from Kontent.ai. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload management asset file](actions/upload-management-asset-file.md) | POST | Uploads an asset file to Kontent.ai. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Add management content item](actions/add-management-content-item.md) | POST | Creates a new content item in Kontent.ai. |
| [Delete management content item](actions/delete-management-content-item.md) | DELETE | Deletes a content item from Kontent.ai. |
| [List management content items](actions/list-management-content-items.md) | GET | Retrieves content items from your Kontent.ai environment. |
| [Retrieve management content item](actions/retrieve-management-content-item.md) | GET | Retrieves a content item from Kontent.ai. |
| [Upsert management content item](actions/upsert-management-content-item.md) | PUT | Upserts a content item in Kontent.ai. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List languages](actions/list-languages.md) | GET | Retrieves languages from your Kontent.ai environment. |

### Taxonomy Group

| Action | Method | Description |
| --- | --- | --- |
| [List taxonomy groups](actions/list-taxonomy-groups.md) | GET | Retrieves taxonomy groups from your Kontent.ai environment. |
| [Retrieve taxonomy group](actions/retrieve-taxonomy-group.md) | GET | Retrieves a taxonomy group from Kontent.ai. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add management language](actions/add-management-language.md) | POST | Creates a new language in Kontent.ai. |
| [List management languages](actions/list-management-languages.md) | GET | Retrieves languages from your Kontent.ai environment. |
| [Modify management language](actions/modify-management-language.md) | PUT | Modifies a language in your Kontent.ai environment. |
| [Retrieve management language](actions/retrieve-management-language.md) | GET | Retrieves a language from your Kontent.ai environment. |

