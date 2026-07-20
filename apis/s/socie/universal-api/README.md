# <img src="https://images.mindcloud.co/apps/icons/socie_1775152331944.png" alt="Socie logo" width="28" height="28"> Socie: Universal API

Socie is a community platform API for managing members, groups, additional fields, notifications, and import triggers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/socie/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://socie.nl
- **Vendor API docs:** https://resources.socie.nl/docs/api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Members](actions/list-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socie/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Additional Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Additional Field](actions/add-additional-field.md) | POST |  |
| [Delete Additional Field](actions/delete-additional-field.md) | DELETE |  |
| [Get Additional Field](actions/get-additional-field.md) | GET |  |
| [List Additional Fields](actions/list-additional-fields.md) | GET |  |
| [Update Additional Field](actions/update-additional-field.md) | PUT |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Group](actions/add-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Group Import

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Importing Groups](actions/trigger-importing-groups.md) | POST |  |

### Group Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Membership](actions/add-group-membership.md) | POST |  |
| [Add Group Memberships in Bulk](actions/add-group-memberships-in-bulk.md) | POST |  |
| [Delete Group Membership](actions/delete-group-membership.md) | DELETE |  |
| [Get Group Membership](actions/get-group-membership.md) | GET |  |
| [List Group Memberships](actions/list-group-memberships.md) | GET |  |
| [Update Group Membership](actions/update-group-membership.md) | PUT |  |
| [Update Group Memberships Order](actions/update-group-memberships-order.md) | PUT |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Member](actions/add-member.md) | POST |  |
| [Add Members in Bulk](actions/add-members-in-bulk.md) | POST |  |
| [Delete Member](actions/delete-member.md) | DELETE |  |
| [Get Member](actions/get-member.md) | GET |  |
| [List Members](actions/list-members.md) | GET |  |
| [Update Member](actions/update-member.md) | PUT |  |

### Member Import

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Importing Members](actions/trigger-importing-members.md) | POST |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send or Schedule Notification](actions/send-or-schedule-notification.md) | POST |  |

