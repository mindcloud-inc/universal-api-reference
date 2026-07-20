# <img src="https://images.mindcloud.co/apps/icons/oneall-icon_1775571949500.png" alt="OneAll logo" width="28" height="28"> OneAll: Universal API

OneAll is a customer identity and social login platform. Use this app to manage users, identities, connections, cloud storage records, SSO sessions, sharing resources, and other documented OneAll API resources through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneAll/latest
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.oneall.com
- **Vendor API docs:** https://docs.oneall.com/api/resources/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Import Access Token](actions/import-access-token.md) | PUT | Imports a user from a social access token in OneAll. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a LoudVoice comment in OneAll. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes a LoudVoice comment from OneAll. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves LoudVoice comment details from OneAll. |
| [List Comments](actions/list-comments.md) | GET | Retrieves all LoudVoice comments from OneAll. |
| [Read Discussion Comments](actions/read-discussion-comments.md) | GET | Retrieves comments for a LoudVoice discussion from OneAll. |
| [Update Comment](actions/update-comment.md) | PUT | Updates a LoudVoice comment in OneAll. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | GET | Retrieves social connection details from OneAll. |
| [List Connections](actions/list-connections.md) | GET | Retrieves all social connections from OneAll. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Read Identity Contacts](actions/read-identity-contacts.md) | GET | Retrieves an identity's social contacts from OneAll. |
| [Read User Contacts](actions/read-user-contacts.md) | GET | Retrieves a user's social contacts from OneAll. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Discussion](actions/create-discussion.md) | POST | Creates a LoudVoice discussion in OneAll. |
| [Delete Discussion](actions/delete-discussion.md) | DELETE | Deletes a LoudVoice discussion from OneAll. |
| [Get Discussion](actions/get-discussion.md) | GET | Retrieves LoudVoice discussion details from OneAll. |
| [List Discussions](actions/list-discussions.md) | GET | Retrieves all LoudVoice discussions from OneAll. |
| [Update Discussion](actions/update-discussion.md) | PUT | Updates a LoudVoice discussion in OneAll. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Publish User Content](actions/publish-user-content.md) | POST | Publishes content to a user's social networks in OneAll. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Cast Vote](actions/cast-vote.md) | PUT | Casts a LoudVoice vote in OneAll. |
| [Delete Vote](actions/delete-vote.md) | DELETE | Deletes a LoudVoice vote from OneAll. |
| [Get Vote](actions/get-vote.md) | GET | Retrieves a LoudVoice vote from OneAll. |
| [List Votes](actions/list-votes.md) | GET | Retrieves all LoudVoice votes from OneAll. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Providers](actions/list-providers.md) | GET | Retrieves all social providers from OneAll. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Delete SSO Session](actions/delete-sso-session.md) | DELETE | Deletes an SSO session from OneAll. |
| [Destroy Identity SSO Session](actions/destroy-identity-sso-session.md) | DELETE | Deletes an identity's SSO session from OneAll. |
| [Get Identity SSO Session](actions/get-identity-sso-session.md) | GET | Retrieves an identity's SSO session from OneAll. |
| [Get SSO Session](actions/get-sso-session.md) | GET | Retrieves SSO session details from OneAll. |
| [List SSO Sessions](actions/list-sso-sessions.md) | GET | Retrieves all SSO sessions from OneAll. |
| [Start Identity SSO Session](actions/start-identity-sso-session.md) | PUT | Starts an SSO session for an identity in OneAll. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Delete Identity](actions/delete-identity.md) | DELETE | Deletes a social identity from OneAll. |
| [Get Identity](actions/get-identity.md) | GET | Retrieves social identity details from OneAll. |
| [List Identities](actions/list-identities.md) | GET | Retrieves all social identities from OneAll. |
| [Relink Identity](actions/relink-identity.md) | PUT | Relinks a social identity to another user in OneAll. |
| [Synchronize Identity](actions/synchronize-identity.md) | PUT | Synchronizes a social identity with its network in OneAll. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Author](actions/create-author.md) | POST | Creates a LoudVoice author in OneAll. |
| [Delete Author](actions/delete-author.md) | DELETE | Deletes a LoudVoice author from OneAll. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from OneAll. |
| [Get Author](actions/get-author.md) | GET | Retrieves LoudVoice author details from OneAll. |
| [Get User](actions/get-user.md) | GET | Retrieves a user's details from OneAll. |
| [List Authors](actions/list-authors.md) | GET | Retrieves all LoudVoice authors from OneAll. |
| [List Users](actions/list-users.md) | GET | Retrieves all site users from OneAll. |
| [Update Author](actions/update-author.md) | PUT | Updates a LoudVoice author in OneAll. |

