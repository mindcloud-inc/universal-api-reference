# <img src="https://images.mindcloud.co/apps/icons/images-1_1775140318335.png" alt="Flotiq logo" width="28" height="28"> Flotiq: Universal API

Manage content types, content objects, media, search, and GraphQL access in Flotiq headless CMS.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flotiq/latest
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flotiq.com/
- **Vendor API docs:** https://flotiq.com/docs/API/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Auth Context](actions/get-auth-context.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-auth-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Auth Context

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Context](actions/get-auth-context.md) | GET | Retrieves your current Flotiq authentication context. |

### Content Object

| Action | Method | Description |
| --- | --- | --- |
| [Archive Content Object](actions/archive-content-object.md) | PUT | Archives a content object in Flotiq. |
| [Batch Archive Content Objects](actions/batch-archive-content-objects.md) | PUT | Archives multiple content objects in Flotiq. |
| [Batch Create Content Objects](actions/batch-create-content-objects.md) | POST | Creates multiple content objects in Flotiq. |
| [Batch Delete Content Objects](actions/batch-delete-content-objects.md) | DELETE | Deletes multiple content objects from Flotiq. |
| [Batch Patch Content Objects](actions/batch-patch-content-objects.md) | PUT | Updates multiple content objects in Flotiq. |
| [Batch Publish Content Objects](actions/batch-publish-content-objects.md) | PUT | Publishes multiple content objects in Flotiq. |
| [Batch Unpublish Content Objects](actions/batch-unpublish-content-objects.md) | PUT | Unpublishes multiple content objects in Flotiq. |
| [Create Content Object](actions/create-content-object.md) | POST | Creates a new content object in Flotiq. |
| [Delete Content Object](actions/delete-content-object.md) | DELETE | Deletes an existing content object from Flotiq. |
| [Get Content Object](actions/get-content-object.md) | GET | Retrieves a content object from Flotiq. |
| [List Content Objects](actions/list-content-objects.md) | GET | Retrieves content objects for a Flotiq content type. |
| [List Removed Content Objects](actions/list-removed-content-objects.md) | GET | Retrieves removed content objects from Flotiq. |
| [Patch Content Object](actions/patch-content-object.md) | PUT | Updates part of a content object in Flotiq. |
| [Publish Content Object](actions/publish-content-object.md) | PUT | Publishes a content object in Flotiq. |
| [Unpublish Content Object](actions/unpublish-content-object.md) | PUT | Unpublishes a content object in Flotiq. |
| [Update Content Object](actions/update-content-object.md) | PUT | Updates an existing content object in Flotiq. |

### Content Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Content Type](actions/create-content-type.md) | POST | Creates a new content type in Flotiq. |
| [Delete Content Type](actions/delete-content-type.md) | DELETE | Deletes an existing content type from Flotiq. |
| [Get Content Type](actions/get-content-type.md) | GET | Retrieves a content type from your Flotiq project. |
| [List Content Types](actions/list-content-types.md) | GET | Retrieves content types from your Flotiq project. |
| [Update Content Type](actions/update-content-type.md) | PUT | Updates an existing content type in Flotiq. |

### Graphql Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GraphQL Query](actions/run-graphql-query.md) | GET | Runs a GraphQL query against Flotiq. |

### Graphql Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get GraphQL Schema](actions/get-graphql-schema.md) | GET | Retrieves the GraphQL schema from Flotiq. |

### Media Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Image](actions/get-media-image.md) | GET | Retrieves a transformed media image from Flotiq. |

### Media Object

| Action | Method | Description |
| --- | --- | --- |
| [Batch Delete Media Objects](actions/batch-delete-media-objects.md) | DELETE | Deletes multiple media objects from Flotiq. |
| [Batch Patch Media Objects](actions/batch-patch-media-objects.md) | PUT | Updates multiple media objects in Flotiq. |
| [Delete Media Object](actions/delete-media-object.md) | DELETE | Deletes an existing media object from Flotiq. |
| [Get Media Object](actions/get-media-object.md) | GET | Retrieves a media object from Flotiq. |
| [List Media Objects](actions/list-media-objects.md) | GET | Retrieves media objects from your Flotiq project. |
| [List Removed Media Objects](actions/list-removed-media-objects.md) | GET | Retrieves removed media objects from Flotiq. |
| [Patch Media Object](actions/patch-media-object.md) | PUT | Updates part of a media object in Flotiq. |
| [Update Media Object](actions/update-media-object.md) | PUT | Updates an existing media object in Flotiq. |

### Media Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload Media](actions/upload-media.md) | POST | Uploads a media file to Flotiq. |

### Media Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Version](actions/get-media-version.md) | GET | Retrieves a media object version from Flotiq. |
| [List Media Versions](actions/list-media-versions.md) | GET | Retrieves versions for a media object in Flotiq. |

### Openapi Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get OpenAPI Schema](actions/get-openapi-schema.md) | GET | Retrieves the OpenAPI schema from Flotiq. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Content](actions/search-content.md) | GET | Searches content objects across your Flotiq project. |

