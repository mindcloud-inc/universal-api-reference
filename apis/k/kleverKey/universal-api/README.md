# <img src="https://images.mindcloud.co/apps/icons/klever-key_1774644390146.png" alt="KleverKey logo" width="28" height="28"> KleverKey: Universal API

Manage users, locks, permissions, and access groups

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kleverKey/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kleverkey.com
- **Vendor API docs:** https://portal.kleverkey.com/documentation/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Access Group](actions/add-access-group.md) | POST |  |
| [Get Access Group](actions/get-access-group.md) | GET |  |
| [List Access Groups](actions/list-access-groups.md) | GET |  |
| [Update Access Group Partially](actions/update-access-group-partially.md) | PUT |  |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Manage Bookings](actions/manage-bookings.md) | POST |  |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Get Invitation](actions/get-invitation.md) | GET |  |
| [Invite User](actions/invite-user.md) | POST |  |
| [List Invitations](actions/list-invitations.md) | GET |  |
| [Resend Invitation](actions/resend-invitation.md) | PUT |  |

### Lock

| Action | Method | Description |
| --- | --- | --- |
| [Get Lock](actions/get-lock.md) | GET |  |
| [List Locks](actions/list-locks.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Get Organization](actions/get-organization.md) | GET |  |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Grant Permission](actions/grant-permission.md) | POST |  |
| [List Permissions](actions/list-permissions.md) | GET |  |
| [Revoke Permission](actions/revoke-permission.md) | DELETE |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add Managed User](actions/add-managed-user.md) | POST |  |
| [Delete Managed User](actions/delete-managed-user.md) | DELETE |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update Managed User](actions/update-managed-user.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

