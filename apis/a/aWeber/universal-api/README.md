# <img src="https://images.mindcloud.co/apps/icons/a-weber_1773169334333.png" alt="AWeber logo" width="28" height="28"> AWeber: Universal API

Manage email lists, subscribers, and campaigns in AWeber

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aWeber/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aweber.com/
- **Vendor API docs:** https://api.aweber.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from AWeber. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from AWeber. |

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled Broadcast](actions/cancel-scheduled-broadcast.md) | PUT | Cancels a scheduled broadcast in AWeber. |
| [Create Broadcast](actions/create-broadcast.md) | POST | Creates a new broadcast in AWeber. |
| [Get Broadcast](actions/get-broadcast.md) | GET | Retrieves a broadcast from AWeber. |
| [List Broadcasts](actions/list-broadcasts.md) | GET | Retrieves broadcasts from AWeber. |
| [Schedule Broadcast](actions/schedule-broadcast.md) | PUT | Schedules a broadcast in AWeber. |
| [Update Broadcast](actions/update-broadcast.md) | PUT | Updates an existing broadcast in AWeber. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Field](actions/add-custom-field.md) | POST | Creates a new custom field in AWeber. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from AWeber. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from AWeber. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from AWeber. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Find Lists](actions/find-lists.md) | GET | Finds lists in AWeber. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from AWeber. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from AWeber. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | POST | Creates a new subscriber in AWeber. |
| [Find Subscribers For Account](actions/find-subscribers-for-account.md) | GET | Finds subscribers in an AWeber account. |
| [Find Subscribers For List](actions/find-subscribers-for-list.md) | GET | Finds subscribers in an AWeber list. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from AWeber. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from AWeber. |
| [Move Subscriber](actions/move-subscriber.md) | PUT | Moves a subscriber in AWeber. |
| [Update Subscriber By ID](actions/update-subscriber-by-id.md) | PUT | Updates an existing subscriber in AWeber. |

### Subscriber Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber Activity](actions/get-subscriber-activity.md) | GET | Retrieves subscriber activity from AWeber. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tags For List](actions/get-tags-for-list.md) | GET | Retrieves tags for a list from AWeber. |

