# <img src="https://images.mindcloud.co/apps/icons/google-slides-logo_1779812244921.png" alt="Google Slides logo" width="28" height="28"> Google Slides: Universal API

Create presentations, collaborate on slides, present live, and share recordings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleSlides/latest
- **Category:** Content & Files / Storage
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workspace.google.com/products/slides/
- **Vendor API docs:** https://developers.google.com/workspace/slides/api/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a presentation page from Google Slides. |

### Page Element

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST | Inserts an image from a public URL onto a slide. |
| [Create Shape](actions/create-shape.md) | POST | Creates a shape or text box on a slide. Add text to it afterwards with Insert Text. |
| [Create Table](actions/create-table.md) | POST | Creates a table on a slide. Fill cells afterwards with Insert Text and a cell location. |
| [Delete Text](actions/delete-text.md) | PUT | Deletes all or part of the text in a shape, text box, placeholder, or table cell. |
| [Insert Text](actions/insert-text.md) | PUT | Inserts text into a shape, text box, placeholder, or table cell on a slide. |

### Presentation

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Presentation](actions/batch-update-presentation.md) | PUT | Applies one or more batch update requests to a presentation in a single atomic call. Use the dedicated actions for common single changes. |
| [Copy Presentation](actions/copy-presentation.md) | POST | Creates a copy of an existing presentation, optionally with a new title. |
| [Create Presentation](actions/create-presentation.md) | POST | Creates a new presentation in Google Slides. |
| [Delete Presentation](actions/delete-presentation.md) | DELETE | Deletes an existing presentation file from Google Slides. |
| [Get Presentation](actions/get-presentation.md) | GET | Retrieves a presentation from Google Slides. |
| [List Presentations](actions/list-presentations.md) | GET | Lists the Google Slides presentations the connection can access, excluding trashed files. |
| [Replace All Shapes with Image](actions/replace-all-shapes-with-image.md) | PUT | Replaces every shape that contains a given text with an image, useful for filling image placeholders in templates. |
| [Replace All Text](actions/replace-all-text.md) | PUT | Replaces every occurrence of a text or pattern across the presentation, useful for filling template placeholders. |
| [Update Presentation](actions/update-presentation.md) | PUT | Updates an existing presentation file in Google Slides. |

### Slide

| Action | Method | Description |
| --- | --- | --- |
| [Create Slide](actions/create-slide.md) | POST | Adds a new slide to a presentation, optionally at a position and with a predefined or existing layout. |
| [Delete Object](actions/delete-object.md) | DELETE | Deletes a slide or page element from a presentation. |
| [Duplicate Object](actions/duplicate-object.md) | POST | Duplicates a slide or page element. A duplicated slide is placed right after the original; a duplicated element stays on the same slide. |
| [Update Slides Position](actions/update-slides-position.md) | PUT | Moves one or more slides to a new position in the presentation. |

### Thumbnail

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Thumbnail](actions/get-page-thumbnail.md) | GET | Retrieves a page thumbnail URL from Google Slides. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the profile of the Google account that authorized the connection. |

