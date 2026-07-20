# <img src="https://images.mindcloud.co/apps/icons/rownd-icon_1775159638442.png" alt="Rownd Data Privacy logo" width="28" height="28"> Rownd Data Privacy: Universal API

App-scoped Rownd Data Privacy and account-management API wrapper for profiles, groups, invites, members, sessions, authentication, and OIDC clients.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rowndDataPrivacy/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rownd.io
- **Vendor API docs:** https://docs.rownd.io/api-reference/authentication/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Sample User Profile Data](actions/get-sample-user-profile-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/get-sample-user-profile-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve JWK Set](actions/retrieve-jwk-set.md) | GET |  |
| [Retrieve OIDC Configuration](actions/retrieve-oidc-configuration.md) | GET |  |

### Group Invites

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Invite](actions/create-group-invite.md) | POST |  |
| [Delete Group Invite](actions/delete-group-invite.md) | DELETE |  |
| [List Group Invites](actions/list-group-invites.md) | GET |  |
| [Retrieve Group Invite](actions/retrieve-group-invite.md) | GET |  |
| [Update Group Invite](actions/update-group-invite.md) | PUT |  |

### Group Members

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Member](actions/create-group-member.md) | POST |  |
| [Delete Group Member](actions/delete-group-member.md) | DELETE |  |
| [List Group Members](actions/list-group-members.md) | GET |  |
| [Retrieve Group Member](actions/retrieve-group-member.md) | GET |  |
| [Update Group Member](actions/update-group-member.md) | PUT |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Retrieve Group](actions/retrieve-group.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Magic Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Magic Link](actions/create-magic-link.md) | POST |  |

### Oidc Clients

| Action | Method | Description |
| --- | --- | --- |
| [Create OIDC Client](actions/create-oidc-client.md) | POST |  |
| [Delete OIDC Client](actions/delete-oidc-client.md) | DELETE |  |
| [List OIDC Clients](actions/list-oidc-clients.md) | GET |  |
| [Retrieve OIDC Client](actions/retrieve-oidc-client.md) | GET |  |
| [Update OIDC Client](actions/update-oidc-client.md) | PUT |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Profile](actions/delete-user-profile.md) | DELETE |  |
| [Get Sample User Profile Data](actions/get-sample-user-profile-data.md) | GET |  |
| [Insert or Update User Profile Data](actions/insert-or-update-user-profile-data.md) | POST |  |
| [List User Profiles](actions/list-user-profiles.md) | GET |  |
| [Retrieve User Profile](actions/retrieve-user-profile.md) | GET |  |
| [Retrieve User Profile Field](actions/retrieve-user-profile-field.md) | GET |  |
| [Update User Profile Data](actions/update-user-profile-data.md) | PUT |  |
| [Update User Profile Field](actions/update-user-profile-field.md) | PUT |  |

### User Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Revoke User Sessions](actions/revoke-user-sessions.md) | PUT |  |

