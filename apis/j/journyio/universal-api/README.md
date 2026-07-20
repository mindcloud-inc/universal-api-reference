# <img src="https://images.mindcloud.co/apps/icons/journyio_1773939923605.png" alt="Journy.io logo" width="28" height="28"> Journy.io: Universal API

Sync users, accounts, and events with Journy.io

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/journyio/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.journy.io
- **Vendor API docs:** https://developers.journy.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Account](actions/create-or-update-account.md) | PUT |  |
| [Delete Account](actions/delete-account.md) | DELETE |  |

### Account Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add Users to Account](actions/add-users-to-account.md) | PUT |  |
| [Remove Users from Account](actions/remove-users-from-account.md) | DELETE |  |

### Account Property

| Action | Method | Description |
| --- | --- | --- |
| [List Account Properties](actions/list-account-properties.md) | GET |  |

### Account Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Account Segments](actions/list-account-segments.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |
| [Track Event](actions/track-event.md) | POST |  |

### Tracking Snippet

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking Snippet](actions/get-tracking-snippet.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update User](actions/create-or-update-user.md) | PUT |  |
| [Delete User](actions/delete-user.md) | DELETE |  |

### User Property

| Action | Method | Description |
| --- | --- | --- |
| [List User Properties](actions/list-user-properties.md) | GET |  |

### User Segment

| Action | Method | Description |
| --- | --- | --- |
| [List User Segments](actions/list-user-segments.md) | GET |  |

### Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET |  |

### Web Activity Link

| Action | Method | Description |
| --- | --- | --- |
| [Link Web Activity to User](actions/link-web-activity-to-user.md) | POST |  |

