# <img src="https://images.mindcloud.co/apps/icons/formester_1774277989046.png" alt="Formester logo" width="28" height="28"> Formester: Universal API

Create forms, collect responses, and run surveys

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formester/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://formester.com
- **Vendor API docs:** https://docs.formester.com/formester-api-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formester/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Formester. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes an existing submission from Formester. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves submission details from Formester. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions from Formester. |

