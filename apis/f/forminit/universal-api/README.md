# <img src="https://images.mindcloud.co/apps/icons/forminit_1773751273410.png" alt="Forminit logo" width="28" height="28"> Forminit: Universal API

Submit forms and manage form submissions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/forminit/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://forminit.com
- **Vendor API docs:** https://forminit.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Submissions](actions/list-submissions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forminit/latest/actions/list-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions for a specific Forminit form. |
| [Submit Form](actions/submit-form.md) | POST | Creates a new submission for a Forminit form. |

