# <img src="https://images.mindcloud.co/apps/icons/chai-logo_1776103830225.png" alt="Chat Aid logo" width="28" height="28"> Chat Aid: Universal API

Ask questions and manage Chat Aid knowledge sources

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatAid/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chataid.com
- **Vendor API docs:** https://docs.chataid.com/api-guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Submit Question](actions/submit-question.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/submit-question?connectionId=$CONNECTION_ID&prompt=What%20is%20our%20refund%20policy%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Completion Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Completion Result](actions/get-completion-result.md) | GET | Retrieves a Chat Aid completion result by prompt ID. |

### Custom Source

| Action | Method | Description |
| --- | --- | --- |
| [Delete Custom Source](actions/delete-custom-source.md) | DELETE | Deletes an existing custom source from Chat Aid. |
| [Delete Custom Sources by IDs](actions/delete-custom-sources-by-ids.md) | DELETE | Deletes custom sources from Chat Aid by IDs or filters. |
| [Get Custom Source](actions/get-custom-source.md) | GET | Retrieves an existing custom source from Chat Aid. |
| [List Custom Sources](actions/list-custom-sources.md) | GET | Retrieves custom sources from your Chat Aid workspace. |
| [Upload Custom Sources](actions/upload-custom-sources.md) | POST | Uploads new custom sources to Chat Aid. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Submit Question](actions/submit-question.md) | GET | Submits a question to Chat Aid for asynchronous completion. |

