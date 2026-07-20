# Swit: Native API Reference

A consolidated summary of Swit's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://tech-support.swit.io/books/swit-java-development-guide
- **API base URL:** `https://openapi.swit.io`

## Authentication

### OAuth2

OAuth2 authorization-code flow for Swit app installation and user-granted API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://openapi.swit.io/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://openapi.swit.io/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `app:install message:write`.

Refresh expired access tokens with a POST request to https://openapi.swit.io/oauth/token.

[Official authentication documentation](https://tech-support.swit.io/books/swit-store-app/page/switapi)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Users To Team](actions/add-users-to-team.md) | `POST team.user.add` | [docs](https://tech-support.swit.io/books/swit-java-development-guide/page/05f97) |
| [Create Message](actions/create-message.md) | `POST message.create` | [docs](https://tech-support.swit.io/books/swit-store-app/page/switapi-Ikx) |
| [Create Team](actions/create-team.md) | `POST team.create` | [docs](https://tech-support.swit.io/books/swit-java-development-guide/page/3fe94) |
| [Create User](actions/create-user.md) | `POST organization.user.create` | [docs](https://tech-support.swit.io/books/swit-java-development-guide/page/6512b) |
| [List Teams](actions/list-teams.md) | `GET user.team.list` | [docs](https://tech-support.swit.io/books/swit-java-development-guide/page/5fd0b) |
| [List Users](actions/list-users.md) | `GET organization.user.list` | [docs](https://tech-support.swit.io/books/swit-java-development-guide/page/9dfcd) |
