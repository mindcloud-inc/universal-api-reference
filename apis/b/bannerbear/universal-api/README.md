# <img src="https://images.mindcloud.co/apps/icons/id-wxg1c0-e-1773433520584_1773433527107.png" alt="Bannerbear logo" width="28" height="28"> Bannerbear: Universal API

Create, manage, and automate image and video generation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bannerbear/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bannerbear.com/
- **Vendor API docs:** https://developers.bannerbear.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authorize](actions/authorize.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/authorize?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | GET | Retrieves account usage from Bannerbear. |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Authorize](actions/authorize.md) | GET | Verifies API authentication with Bannerbear. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Bannerbear. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves collection from Bannerbear. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Bannerbear. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST | Creates a new image in Bannerbear. |
| [Get Image](actions/get-image.md) | GET | Retrieves image from Bannerbear. |
| [List Images](actions/list-images.md) | GET | Retrieves images from Bannerbear. |

### Movie

| Action | Method | Description |
| --- | --- | --- |
| [Create Movie](actions/create-movie.md) | POST | Creates a new movie in Bannerbear. |
| [Get Movie](actions/get-movie.md) | GET | Retrieves movie from Bannerbear. |
| [List Movies](actions/list-movies.md) | GET | Retrieves movies from Bannerbear. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Bannerbear. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Bannerbear. |
| [Duplicate Template](actions/duplicate-template.md) | POST | Duplicates a template in Bannerbear. |
| [Get Template](actions/get-template.md) | GET | Retrieves template from Bannerbear. |
| [Import Templates](actions/import-templates.md) | POST | Imports templates into Bannerbear. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Bannerbear. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Bannerbear. |

### Template Set

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Set](actions/create-template-set.md) | POST | Creates a new template set in Bannerbear. |
| [Get Template Set](actions/get-template-set.md) | GET | Retrieves template set from Bannerbear. |
| [List Template Sets](actions/list-template-sets.md) | GET | Retrieves template sets from Bannerbear. |
| [Update Template Set](actions/update-template-set.md) | PUT | Updates an existing template set in Bannerbear. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video](actions/create-video.md) | POST | Creates a new video in Bannerbear. |
| [Get Video](actions/get-video.md) | GET | Retrieves video from Bannerbear. |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from Bannerbear. |
| [Update Video](actions/update-video.md) | PUT | Updates an existing video in Bannerbear. |

### Video Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Template](actions/create-video-template.md) | POST | Creates a new video template in Bannerbear. |
| [Get Video Template](actions/get-video-template.md) | GET | Retrieves video template from Bannerbear. |
| [List Video Templates](actions/list-video-templates.md) | GET | Retrieves video templates from Bannerbear. |

