# MemberVault: Native API Reference

A consolidated summary of MemberVault's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced
- **API base URL:** `https://{accountName}.mvsite.app/api`

## Authentication

### API Key

Connect with your MemberVault API key and account subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Account Name:** `accountName` · required · Your MemberVault account subdomain from your site URL.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.membervault.co/en/articles/9163897-membervault-api-endpoints-for-custom-integrations)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User to Product](actions/add-user-to-product.md) | `GET /add_user` | [docs](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced) |
| [Delete User](actions/delete-user.md) | `GET /delete_user` | [docs](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced) |
| [List Products](actions/list-products.md) | `GET /get_courses` | [docs](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced) |
| [Remove User from Product](actions/remove-user-from-product.md) | `GET /remove_user` | [docs](https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced) |
