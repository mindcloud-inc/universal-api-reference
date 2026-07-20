# <img src="https://images.mindcloud.co/apps/icons/favicon-16_1775507404095.png" alt="Aspose logo" width="28" height="28"> Aspose: Universal API

Use Aspose Cloud APIs to create, convert, render, and manipulate documents, presentations, images, and other file formats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aspose/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aspose.cloud/products/
- **Vendor API docs:** https://docs.aspose.cloud/slides/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Information](actions/get-api-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/get-api-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Document Property

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Properties](actions/add-custom-properties.md) | POST | Creates custom document properties in Aspose. |
| [Delete Document Property](actions/delete-document-property.md) | DELETE | Deletes a document property from a presentation in Aspose. |
| [Get Document Property](actions/get-document-property.md) | GET | Retrieves a document property from a presentation in Aspose. |
| [List Document Properties](actions/list-document-properties.md) | GET | Retrieves document properties from a presentation in Aspose. |
| [Update Document Property](actions/update-document-property.md) | PUT | Updates a document property in a presentation in Aspose. |

### Placeholder

| Action | Method | Description |
| --- | --- | --- |
| [List Slide Placeholders](actions/list-slide-placeholders.md) | GET | Retrieves placeholders from a slide in Aspose. |

### Presentation

| Action | Method | Description |
| --- | --- | --- |
| [Create Presentation](actions/create-presentation.md) | POST | Creates a new presentation in Aspose. |
| [Get Presentation](actions/get-presentation.md) | GET | Retrieves details for a presentation in Aspose. |

### Shape

| Action | Method | Description |
| --- | --- | --- |
| [Create Shape](actions/create-shape.md) | POST | Creates a new shape in a slide in Aspose. |
| [Delete Shape](actions/delete-shape.md) | DELETE | Deletes a shape from a slide in Aspose. |
| [Get Shape](actions/get-shape.md) | GET | Retrieves a shape from a slide in Aspose. |
| [List Shapes](actions/list-shapes.md) | GET | Retrieves shapes from a slide in Aspose. |

### Slide

| Action | Method | Description |
| --- | --- | --- |
| [Copy Slide](actions/copy-slide.md) | POST | Copies slides within a presentation in Aspose. |
| [Create Slide](actions/create-slide.md) | POST | Creates a new slide in a presentation in Aspose. |
| [Delete Slide](actions/delete-slide.md) | DELETE | Deletes a slide from a presentation in Aspose. |
| [Delete Slides](actions/delete-slides.md) | DELETE | Deletes existing slides from a presentation in Aspose. |
| [Get Slide](actions/get-slide.md) | GET | Retrieves a slide from a presentation in Aspose. |
| [List Slides](actions/list-slides.md) | GET | Retrieves slides from a presentation in Aspose. |
| [Move Slide](actions/move-slide.md) | PUT | Moves a slide within a presentation in Aspose. |

### Slides Api

| Action | Method | Description |
| --- | --- | --- |
| [Get API Information](actions/get-api-information.md) | GET | Retrieves Slides API information from Aspose. |

### Text Item

| Action | Method | Description |
| --- | --- | --- |
| [List Presentation Text Items](actions/list-presentation-text-items.md) | GET | Retrieves text items from a presentation in Aspose. |
| [List Slide Text Items](actions/list-slide-text-items.md) | GET | Retrieves text items from a slide in Aspose. |
| [Replace Presentation Text](actions/replace-presentation-text.md) | PUT | Replaces text throughout a presentation in Aspose. |
| [Replace Slide Text](actions/replace-slide-text.md) | PUT | Replaces text within a slide in Aspose. |

