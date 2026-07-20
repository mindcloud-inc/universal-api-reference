# <img src="https://images.mindcloud.co/apps/icons/google-forms-default_1779719542830.png" alt="Google Forms logo" width="28" height="28"> Google Forms: Universal API

Create forms, collect responses, share surveys, and analyze results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleForms/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docs.google.com/forms/
- **Vendor API docs:** https://developers.google.com/workspace/forms/api/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Form](actions/get-form.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form?connectionId=$CONNECTION_ID&formId=1FAIpQLSdExampleFormId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Add Questions To Form](actions/add-questions-to-form.md) | PUT | Adds multiple questions to a form in Google Forms. |
| [Batch Update Form](actions/batch-update-form.md) | PUT | Applies batch updates to a form in Google Forms. |
| [Create Choice Question](actions/create-choice-question.md) | PUT | Creates a choice question in Google Forms. |
| [Create Date Question](actions/create-date-question.md) | PUT | Creates a date question in Google Forms. |
| [Create Form](actions/create-form.md) | POST | Creates a new empty form in Google Forms. |
| [Create Form Watch](actions/create-form-watch.md) | POST | Creates a new seven-day form watch in Google Forms. |
| [Create Image Item](actions/create-image-item.md) | PUT | Creates an image item in Google Forms. |
| [Create Question Group Item](actions/create-question-group-item.md) | PUT | Creates a question group item in Google Forms. |
| [Create Question Item](actions/create-question-item.md) | PUT | Creates a question item in Google Forms. |
| [Create Rating Question](actions/create-rating-question.md) | PUT | Creates a rating question in Google Forms. |
| [Create Scale Question](actions/create-scale-question.md) | PUT | Creates a scale question in Google Forms. |
| [Create Section Header Item](actions/create-section-header-item.md) | PUT | Creates a section header item in Google Forms. |
| [Create Text Item](actions/create-text-item.md) | PUT | Creates a static text item in Google Forms. |
| [Create Text Question](actions/create-text-question.md) | PUT | Creates a text question in Google Forms. |
| [Create Time Question](actions/create-time-question.md) | PUT | Creates a time question in Google Forms. |
| [Create Video Item](actions/create-video-item.md) | PUT | Creates a video item in Google Forms. |
| [Delete Form Item](actions/delete-form-item.md) | PUT | Deletes an existing form item from Google Forms. |
| [Delete Form Watch](actions/delete-form-watch.md) | DELETE | Deletes an existing form watch from Google Forms. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Google Forms. |
| [Get Form Response](actions/get-form-response.md) | GET | Retrieves a form response from Google Forms. |
| [List Form Responses](actions/list-form-responses.md) | GET | Retrieves form responses from Google Forms. |
| [List Form Watches](actions/list-form-watches.md) | GET | Retrieves form watches from Google Forms. |
| [Move Form Item](actions/move-form-item.md) | PUT | Moves a form item within Google Forms. |
| [Move Question To Section](actions/move-question-to-section.md) | PUT | Moves a question into a section in Google Forms. |
| [Renew Form Watch](actions/renew-form-watch.md) | PUT | Renews a form watch in Google Forms for seven days. |
| [Set Collect Email](actions/set-collect-email.md) | PUT | Updates a form's email collection settings in Google Forms. |
| [Set Publish Settings](actions/set-publish-settings.md) | PUT | Updates a form's publish settings in Google Forms. |
| [Set Quiz Mode](actions/set-quiz-mode.md) | PUT | Updates a form's quiz mode in Google Forms. |
| [Update Form Info](actions/update-form-info.md) | PUT | Updates a form's title or description in Google Forms. |
| [Update Form Item](actions/update-form-item.md) | PUT | Updates an existing form item in Google Forms. |
| [Update Form Settings](actions/update-form-settings.md) | PUT | Updates a form's settings in Google Forms. |

