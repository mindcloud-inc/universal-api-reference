# <img src="https://images.mindcloud.co/apps/icons/screenshot-at-apr-27-14-42-59_1777311789659.png" alt="Atriomail logo" width="28" height="28"> Atriomail: Universal API

White-label email hosting and provisioning API for resellers and agencies, including mailbox, domain, forwarder, catch-all, quota, migration, and user management workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/atriomail/latest
- **Category:** Communication / Email Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://atriomail.com/
- **Vendor API docs:** https://system.atriomail.com/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Catch-all

| Action | Method | Description |
| --- | --- | --- |
| [Get Catch-All](actions/get-catch-all.md) | GET |  |
| [List Catch-Alls](actions/list-catch-alls.md) | GET |  |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST |  |
| [Get Domain](actions/get-domain.md) | GET |  |
| [List Domains](actions/list-domains.md) | GET |  |

### Forwarder

| Action | Method | Description |
| --- | --- | --- |
| [Get Forwarder](actions/get-forwarder.md) | GET |  |
| [List Forwarders](actions/list-forwarders.md) | GET |  |

### Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailbox](actions/create-mailbox.md) | POST |  |
| [Delete Mailbox](actions/delete-mailbox.md) | DELETE |  |
| [Get Mailbox](actions/get-mailbox.md) | GET |  |
| [List Domain Mailboxes](actions/list-domain-mailboxes.md) | GET |  |
| [List Mailboxes](actions/list-mailboxes.md) | GET |  |
| [Update Mailbox](actions/update-mailbox.md) | PUT |  |

### Migration

| Action | Method | Description |
| --- | --- | --- |
| [List Migrations](actions/list-migrations.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

