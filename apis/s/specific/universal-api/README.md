# <img src="https://images.mindcloud.co/apps/icons/specific_1775668848089.png" alt="Specific logo" width="28" height="28"> Specific: Universal API

Specific: Manage surveys, conversations, users, and company data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/specific/latest
- **Category:** Support / Customer Success
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://specific.app
- **Vendor API docs:** https://public-api.specific.app/docs/introduction/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace](actions/get-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in Specific. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes a company from Specific. |
| [Get Company By Exact Name](actions/get-company-by-exact-name.md) | GET | Retrieves a company from Specific by exact name. |
| [Get Company By ID](actions/get-company-by-id.md) | GET | Retrieves a company from Specific by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves a list of companies from Specific. |
| [Search Companies By Name Contains](actions/search-companies-by-name-contains.md) | GET | Finds companies in Specific by partial name. |
| [Search Companies By Name Starts With](actions/search-companies-by-name-starts-with.md) | GET | Finds companies in Specific by name prefix. |
| [Update Company By ID](actions/update-company-by-id.md) | PUT | Updates a company in Specific by ID. |
| [Upsert Company By ID](actions/upsert-company-by-id.md) | PUT | Creates or updates a company in Specific by ID. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves a list of conversations from Specific. |
| [List Conversations By Source IDs](actions/list-conversations-by-source-ids.md) | GET | Retrieves conversations from Specific by source IDs. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves a list of custom fields from Specific. |
| [List Company Attributes](actions/list-company-attributes.md) | GET | Retrieves company custom fields from Specific. |
| [List Conversation Attributes](actions/list-conversation-attributes.md) | GET | Retrieves conversation custom fields from Specific. |
| [List User Attributes](actions/list-user-attributes.md) | GET | Retrieves user custom fields from Specific. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves a list of sources from Specific. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves a list of surveys from Specific. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in Specific. |
| [Delete User By Email](actions/delete-user-by-email.md) | DELETE | Deletes a user from Specific by email. |
| [Delete User By ID](actions/delete-user-by-id.md) | DELETE | Deletes a user from Specific by ID. |
| [Get User By Email](actions/get-user-by-email.md) | GET | Retrieves a user from Specific by email. |
| [Get User By ID](actions/get-user-by-id.md) | GET | Retrieves a user from Specific by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Specific. |
| [Search Users By Email Contains](actions/search-users-by-email-contains.md) | GET | Finds users in Specific by partial email. |
| [Search Users By ID Contains](actions/search-users-by-id-contains.md) | GET | Finds users in Specific by partial ID. |
| [Update User By Email](actions/update-user-by-email.md) | PUT | Updates a user in Specific by email. |
| [Update User By ID](actions/update-user-by-id.md) | PUT | Updates a user in Specific by ID. |
| [Upsert User By Email](actions/upsert-user-by-email.md) | PUT | Creates or updates a user in Specific by email. |
| [Upsert User By ID](actions/upsert-user-by-id.md) | PUT | Creates or updates a user in Specific by ID. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Specific. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves the current workspace from Specific. |

