# <img src="https://images.mindcloud.co/apps/icons/images-1_1773185346463.png" alt="Pushover logo" width="28" height="28"> Pushover: Universal API

Send Pushover notifications and validate users, groups, and devices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushover/latest
- **Category:** Communication / Team Messaging
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pushover.net/
- **Vendor API docs:** https://pushover.net/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate User or Group](actions/validate-user-or-group.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/validate-user-or-group?connectionId=$CONNECTION_ID&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### App Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get App Limits](actions/get-app-limits.md) | GET |  |

### Glance

| Action | Method | Description |
| --- | --- | --- |
| [Update Glance](actions/update-glance.md) | PUT |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Rename Group](actions/rename-group.md) | PUT |  |

### Group User

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Group](actions/add-user-to-group.md) | POST |  |
| [Disable Group User](actions/disable-group-user.md) | PUT |  |
| [Enable Group User](actions/enable-group-user.md) | PUT |  |
| [Remove User from Group](actions/remove-user-from-group.md) | DELETE |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST |  |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Emergency Receipt](actions/cancel-emergency-receipt.md) | PUT |  |
| [Cancel Emergency Receipts by Tag](actions/cancel-emergency-receipts-by-tag.md) | PUT |  |
| [Get Receipt Status](actions/get-receipt-status.md) | GET |  |

### Sound

| Action | Method | Description |
| --- | --- | --- |
| [List Sounds](actions/list-sounds.md) | GET |  |

### Subscription User Key

| Action | Method | Description |
| --- | --- | --- |
| [Migrate Subscription User Key](actions/migrate-subscription-user-key.md) | POST |  |

### User Or Group

| Action | Method | Description |
| --- | --- | --- |
| [Validate User or Group](actions/validate-user-or-group.md) | GET |  |

