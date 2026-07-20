# <img src="https://images.mindcloud.co/apps/icons/moaform_1774549195891.png" alt="Moaform logo" width="28" height="28"> Moaform: Universal API

Create forms, collect responses, and manage webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moaform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moaform.com
- **Vendor API docs:** https://help.moaform.com/hc/en-us/sections/28248280913561-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download Submitted Attachment](actions/download-submitted-attachment.md) | GET | Retrieves a submitted attachment from Moaform. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from your Moaform account. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your Moaform account. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Delete Response](actions/delete-response.md) | DELETE | Deletes a form response from Moaform. |
| [List Form Responses](actions/list-form-responses.md) | GET | Retrieves responses for a form in Moaform. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook for a form in Moaform. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from a form in Moaform. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks for a form in Moaform. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a form webhook in Moaform. |

