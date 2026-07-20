# <img src="https://images.mindcloud.co/apps/icons/rapido-form_1774980895195.png" alt="RapidoForm logo" width="28" height="28"> RapidoForm: Universal API

Create forms, manage questions and themes, capture responses, and send webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rapidoForm/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rapidoform.com
- **Vendor API docs:** https://www.rapidoform.com/developers/docs/get-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in RapidoForm. |
| [List Forms](actions/list-forms.md) | GET | Retrieves all available forms from RapidoForm. |

### Questions

| Action | Method | Description |
| --- | --- | --- |
| [Create Question](actions/create-question.md) | POST | Creates a new question in RapidoForm. |

### Themes

| Action | Method | Description |
| --- | --- | --- |
| [Create Theme](actions/create-theme.md) | POST | Creates a new theme in RapidoForm. |
| [List My Themes](actions/list-my-themes.md) | GET | Retrieves your saved themes from RapidoForm. |
| [List Theme Gallery](actions/list-theme-gallery.md) | GET | Retrieves all gallery themes from RapidoForm. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook for RapidoForm form submissions. |

