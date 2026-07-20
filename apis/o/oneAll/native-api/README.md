# OneAll: Native API Reference

A consolidated summary of OneAll's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://docs.oneall.com/api/resources/
- **API base URL:** `https://mindcloudco.api.oneall.com`

## Authentication

### Basic Auth

Use your OneAll site public key as the username and your site private key as the password. Requests are sent to your site subdomain at <subdomain>.api.oneall.com.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.oneall.com/api/basic/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `entries_per_page` in the query string to set the page size (default 250; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cast Vote](actions/cast-vote.md) | `PUT /loudvoice/votes/comments/<comment_token>/authors/<author_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/votes/cast/) |
| [Create Author](actions/create-author.md) | `POST /loudvoice/authors.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/authors/create/) |
| [Create Comment](actions/create-comment.md) | `POST /loudvoice/comments.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/comment/create/) |
| [Create Discussion](actions/create-discussion.md) | `POST /loudvoice/discussions.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/discussions/create/) |
| [Delete Author](actions/delete-author.md) | `DELETE /loudvoice/authors/<author_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/authors/delete/) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /loudvoice/comments/<comment_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/comment/delete/) |
| [Delete Discussion](actions/delete-discussion.md) | `DELETE /loudvoice/discussions/<discussion_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/discussions/delete/) |
| [Delete Identity](actions/delete-identity.md) | `DELETE /identities/<identity_token>.json` | [docs](https://docs.oneall.com/api/resources/identities/delete-identity/) |
| [Delete SSO Session](actions/delete-sso-session.md) | `DELETE /sso/sessions/<sso_session_token>.json` | [docs](https://docs.oneall.com/api/resources/sso/delete-session/) |
| [Delete User](actions/delete-user.md) | `DELETE /users/<user_token>.json` | [docs](https://docs.oneall.com/api/resources/users/delete-user/) |
| [Delete Vote](actions/delete-vote.md) | `DELETE /loudvoice/votes/comments/<comment_token>/authors/<author_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/votes/delete/) |
| [Destroy Identity SSO Session](actions/destroy-identity-sso-session.md) | `DELETE /sso/sessions/identities/<identity_token>.json` | [docs](https://docs.oneall.com/api/resources/sso/identity/destroy-session/) |
| [Get Author](actions/get-author.md) | `GET /loudvoice/authors/<author_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/authors/read/) |
| [Get Comment](actions/get-comment.md) | `GET /loudvoice/comments/<comment_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/comment/read/) |
| [Get Connection](actions/get-connection.md) | `GET /connections/<connection_token>.json` | [docs](https://docs.oneall.com/api/resources/connections/read-connection-details/) |
| [Get Discussion](actions/get-discussion.md) | `GET /loudvoice/discussions/<discussion_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/discussions/read/) |
| [Get Identity](actions/get-identity.md) | `GET /identities/<identity_token>.json` | [docs](https://docs.oneall.com/api/resources/identities/read-identity-details/) |
| [Get Identity SSO Session](actions/get-identity-sso-session.md) | `GET /sso/sessions/identities/<identity_token>.json` | [docs](https://docs.oneall.com/api/resources/sso/identity/read-session/) |
| [Get SSO Session](actions/get-sso-session.md) | `GET /sso/sessions/<sso_session_token>.json` | [docs](https://docs.oneall.com/api/resources/sso/read-session-details/) |
| [Get User](actions/get-user.md) | `GET /users/<user_token>.json` | [docs](https://docs.oneall.com/api/resources/users/read-user-details/) |
| [Get Vote](actions/get-vote.md) | `GET /loudvoice/votes/comments/<comment_token>/authors/<author_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/votes/read/) |
| [Import Access Token](actions/import-access-token.md) | `PUT /users.json` | [docs](https://docs.oneall.com/api/resources/users/import-user/) |
| [List Authors](actions/list-authors.md) | `GET /loudvoice/authors.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/authors/list/) |
| [List Comments](actions/list-comments.md) | `GET /loudvoice/comments.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/comment/list/) |
| [List Connections](actions/list-connections.md) | `GET /connections.json` | [docs](https://docs.oneall.com/api/resources/connections/list-all-connections/) |
| [List Discussions](actions/list-discussions.md) | `GET /loudvoice/discussions.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/discussions/list/) |
| [List Identities](actions/list-identities.md) | `GET /identities.json` | [docs](https://docs.oneall.com/api/resources/identities/list-all-identities/) |
| [List Providers](actions/list-providers.md) | `GET /providers.json` | [docs](https://docs.oneall.com/api/resources/providers/list-all-providers/) |
| [List SSO Sessions](actions/list-sso-sessions.md) | `GET /sso/sessions.json` | [docs](https://docs.oneall.com/api/resources/sso/list-all-sessions/) |
| [List Users](actions/list-users.md) | `GET /users.json` | [docs](https://docs.oneall.com/api/resources/users/list-all-users/) |
| [List Votes](actions/list-votes.md) | `GET /loudvoice/votes.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/votes/list/) |
| [Publish User Content](actions/publish-user-content.md) | `POST /users/<user_token>/publish.json` | [docs](https://docs.oneall.com/api/resources/users/write-to-users-wall/) |
| [Read Discussion Comments](actions/read-discussion-comments.md) | `GET /loudvoice/comments/<discussion_token>/comments.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/discussions/comments/) |
| [Read Identity Contacts](actions/read-identity-contacts.md) | `GET /identities/<identity_token>/contacts.json` | [docs](https://docs.oneall.com/api/resources/identities/read-contacts/) |
| [Read User Contacts](actions/read-user-contacts.md) | `GET /users/<user_token>/contacts.json` | [docs](https://docs.oneall.com/api/resources/users/read-contacts/) |
| [Relink Identity](actions/relink-identity.md) | `PUT /identities/<identity_token>/link.json` | [docs](https://docs.oneall.com/api/resources/identities/relink-identity/) |
| [Start Identity SSO Session](actions/start-identity-sso-session.md) | `PUT /sso/sessions/identities/<identity_token>.json` | [docs](https://docs.oneall.com/api/resources/sso/identity/start-session/) |
| [Synchronize Identity](actions/synchronize-identity.md) | `PUT /identities/<identity_token>/synchronize.json` | [docs](https://docs.oneall.com/api/resources/identities/synchronize-identity/) |
| [Update Author](actions/update-author.md) | `PUT /loudvoice/authors/<author_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/authors/update/) |
| [Update Comment](actions/update-comment.md) | `PUT /loudvoice/comments/<comment_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/comment/update/) |
| [Update Discussion](actions/update-discussion.md) | `PUT /loudvoice/discussions/<discussion_token>.json` | [docs](https://docs.oneall.com/api/resources/loudvoice/discussions/update/) |
