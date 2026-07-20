# <img src="https://images.mindcloud.co/apps/icons/indy-forms_1775661764554.png" alt="IndyForms logo" width="28" height="28"> IndyForms: Universal API

Access IndyForms forms, records, users, and webhooks through the official Public API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/indyForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://indyforms.com/api/
- **Vendor API docs:** https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Record](actions/get-record.md) | GET |  |
| [List Form Records](actions/list-form-records.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

