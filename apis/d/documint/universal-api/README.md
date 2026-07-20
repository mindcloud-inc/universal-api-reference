# <img src="https://images.mindcloud.co/apps/icons/documint_1773852324047.png" alt="Documint logo" width="28" height="28"> Documint: Universal API

Generate documents from Documint templates, list and manage templates, and merge data into downloadable documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documint/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://documint.me/
- **Vendor API docs:** https://documenter.getpostman.com/view/11741160/TVK5cLxQ

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documint/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Merge Template](actions/merge-template.md) | POST | Creates a document from a template in Documint. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Delete Template](actions/delete-template.md) | DELETE | Permanently deletes an existing template from Documint. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Documint by ID. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from Documint. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Documint. |

