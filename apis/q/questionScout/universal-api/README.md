# <img src="https://images.mindcloud.co/apps/icons/question-scout_1774359087299.png" alt="QuestionScout logo" width="28" height="28"> QuestionScout: Universal API

QuestionScout is a forms and surveys platform. The currently verified public API surface for MindCloud is the WordPress forms endpoint plus QuestionScout's documented trigger/webhook surfaces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/questionScout/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.questionscout.com/
- **Vendor API docs:** https://support.questionscout.com/category/31-sharing-embedding

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionScout/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your QuestionScout account. |

