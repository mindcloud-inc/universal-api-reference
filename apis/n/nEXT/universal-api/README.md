# <img src="https://images.mindcloud.co/apps/icons/next-icon_1775742754106.png" alt="NEXT logo" width="28" height="28"> NEXT: Universal API

NEXT lets you query and create customer-feedback data within your teamspace, including accounts, highlights, playlists, projects, recordings, AI artifacts, automations, integrations, tags, users, views, and related tenant resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nEXT/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nextapp.co/
- **Vendor API docs:** https://developer.nextapp.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in NEXT. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an existing account from NEXT. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from NEXT. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from NEXT. |
| [Search Accounts](actions/search-accounts.md) | GET | Finds accounts in NEXT by search term. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in NEXT. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in NEXT. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from NEXT. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from NEXT. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from NEXT. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in NEXT. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Prompt Template](actions/create-ai-prompt-template.md) | POST | Creates a new AI prompt template in NEXT. |
| [Delete AI Prompt Template](actions/delete-ai-prompt-template.md) | DELETE | Deletes an existing AI prompt template from NEXT. |
| [Get AI Prompt Template](actions/get-ai-prompt-template.md) | GET | Retrieves an AI prompt template from NEXT. |
| [List AI Prompt Templates](actions/list-ai-prompt-templates.md) | GET | Retrieves AI prompt templates from NEXT. |
| [Update AI Prompt Template](actions/update-ai-prompt-template.md) | PUT | Updates an existing AI prompt template in NEXT. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Thread](actions/create-ai-thread.md) | POST | Creates a new AI thread in NEXT. |
| [Delete AI Thread](actions/delete-ai-thread.md) | DELETE | Deletes an existing AI thread from NEXT. |
| [Get AI Thread](actions/get-ai-thread.md) | GET | Retrieves an AI thread from NEXT. |
| [List AI Threads](actions/list-ai-threads.md) | GET | Retrieves AI threads from NEXT. |
| [Update AI Thread](actions/update-ai-thread.md) | PUT | Updates an existing AI thread in NEXT. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Query](actions/create-ai-query.md) | POST | Creates a new AI query in NEXT. |
| [Delete AI Query](actions/delete-ai-query.md) | DELETE | Deletes an existing AI query from NEXT. |
| [Get AI Query](actions/get-ai-query.md) | GET | Retrieves an AI query from NEXT. |
| [Update AI Query](actions/update-ai-query.md) | PUT | Updates an existing AI query in NEXT. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Rule](actions/create-ai-rule.md) | POST | Creates a new AI rule in NEXT. |
| [Delete AI Rule](actions/delete-ai-rule.md) | DELETE | Deletes an existing AI rule from NEXT. |
| [Get AI Rule](actions/get-ai-rule.md) | GET | Retrieves an AI rule from NEXT. |
| [List AI Rules](actions/list-ai-rules.md) | GET | Retrieves AI rules from NEXT. |
| [Update AI Rule](actions/update-ai-rule.md) | PUT | Updates an existing AI rule in NEXT. |

