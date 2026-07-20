# <img src="https://images.mindcloud.co/apps/icons/youform_1773441321921.png" alt="Youform logo" width="28" height="28"> Youform: Universal API

Manage Youform forms, submissions, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/youform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://youform.com
- **Vendor API docs:** https://youform.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youform/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Youform. |
| [List Forms](actions/list-forms.md) | GET | Lists forms in Youform. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves your profile from Youform. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Lists submissions for a form in Youform. |
| [Set Submission Refill Link](actions/set-submission-refill-link.md) | PUT | Enables or disables a submission refill link in Youform. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Youform. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Youform. |

