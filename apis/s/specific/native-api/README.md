# Specific: Native API Reference

A consolidated summary of Specific's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://public-api.specific.app/docs/introduction/welcome
- **API base URL:** `https://public-api.specific.app/graphql`

## Authentication

### API Key

Use a Specific personal API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://public-api.specific.app/docs/introduction/welcome)

## API conventions

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/createCompany) |
| [Create User](actions/create-user.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/createUser) |
| [Delete Company](actions/delete-company.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/deleteCompany) |
| [Delete User By Email](actions/delete-user-by-email.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/deleteUser) |
| [Delete User By ID](actions/delete-user-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/deleteUser) |
| [Get Company By Exact Name](actions/get-company-by-exact-name.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/companies) |
| [Get Company By ID](actions/get-company-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/companies) |
| [Get User By Email](actions/get-user-by-email.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/users) |
| [Get User By ID](actions/get-user-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/users) |
| [Get Workspace](actions/get-workspace.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/myWorkspace) |
| [List Attributes](actions/list-attributes.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/attributes) |
| [List Companies](actions/list-companies.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/companies) |
| [List Company Attributes](actions/list-company-attributes.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/attributes) |
| [List Conversation Attributes](actions/list-conversation-attributes.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/attributes) |
| [List Conversations](actions/list-conversations.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/conversations) |
| [List Conversations By Source IDs](actions/list-conversations-by-source-ids.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/conversations) |
| [List Sources](actions/list-sources.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/sources) |
| [List Surveys](actions/list-surveys.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/surveys) |
| [List User Attributes](actions/list-user-attributes.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/attributes) |
| [List Users](actions/list-users.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/users) |
| [List Webhooks](actions/list-webhooks.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/webhooks) |
| [Search Companies By Name Contains](actions/search-companies-by-name-contains.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/companies) |
| [Search Companies By Name Starts With](actions/search-companies-by-name-starts-with.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/companies) |
| [Search Users By Email Contains](actions/search-users-by-email-contains.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/users) |
| [Search Users By ID Contains](actions/search-users-by-id-contains.md) | `POST` | [docs](https://public-api.specific.app/docs/queries/users) |
| [Update Company By ID](actions/update-company-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/updateCompany) |
| [Update User By Email](actions/update-user-by-email.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/updateUser) |
| [Update User By ID](actions/update-user-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/updateUser) |
| [Upsert Company By ID](actions/upsert-company-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/createOrUpdateCompany) |
| [Upsert User By Email](actions/upsert-user-by-email.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/createOrUpdateUser) |
| [Upsert User By ID](actions/upsert-user-by-id.md) | `POST` | [docs](https://public-api.specific.app/docs/mutations/createOrUpdateUser) |
