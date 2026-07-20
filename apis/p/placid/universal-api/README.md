# <img src="https://images.mindcloud.co/apps/icons/placid_1773785001146.png" alt="Placid logo" width="28" height="28"> Placid: Universal API

Generate images, PDFs, and videos from templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/placid/latest
- **Category:** Marketing
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://placid.app
- **Vendor API docs:** https://placid.app/docs/2.0/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placid/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Placid. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from Placid. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from Placid. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Placid. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in Placid. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST | Creates a new image in Placid from a template. |
| [Delete Image](actions/delete-image.md) | DELETE | Deletes an image render from Placid. |
| [Get Image](actions/get-image.md) | GET | Retrieves an image render from Placid. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [Upload Media](actions/upload-media.md) | POST | Uploads media to Placid and returns reusable file URLs. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF](actions/create-pdf.md) | POST | Creates a new PDF in Placid from template pages. |
| [Delete PDF](actions/delete-pdf.md) | DELETE | Deletes a PDF render from Placid. |
| [Get PDF](actions/get-pdf.md) | GET | Retrieves a PDF render from Placid. |
| [Merge PDFs](actions/merge-pdfs.md) | POST | Merges PDFs in Placid from source URLs. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Placid. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Placid. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Placid. |
| [List Templates](actions/list-templates.md) | GET | Finds templates in Placid by collection, title, or tag. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Placid. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video](actions/create-video.md) | POST | Creates a new video in Placid from template clips. |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes a video render from Placid. |
| [Get Video](actions/get-video.md) | GET | Retrieves a video render from Placid. |

