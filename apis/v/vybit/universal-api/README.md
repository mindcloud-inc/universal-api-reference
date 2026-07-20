# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-18-at-15_1773857355493.png" alt="Vybit logo" width="28" height="28"> Vybit: Universal API

Vybit lets you create, trigger, subscribe to, and manage custom sound notifications and reminders.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vybit/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vybit.net
- **Vendor API docs:** https://developer.vybit.net/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Legacy Trigger Response

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Vybit Notification (Legacy OAuth)](actions/trigger-vybit-notification-legacy-oauth.md) | POST |  |

### Legacy Vybit

| Action | Method | Description |
| --- | --- | --- |
| [List Vybits (Legacy OAuth)](actions/list-vybits-legacy-oauth.md) | GET |  |

### Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Log Entry](actions/get-log-entry.md) | GET |  |
| [List All Logs](actions/list-all-logs.md) | GET |  |
| [List Logs for Owned Vybit](actions/list-logs-for-owned-vybit.md) | GET |  |
| [List Logs for Subscription Following](actions/list-logs-for-subscription-following.md) | GET |  |

### Oauth Token Status

| Action | Method | Description |
| --- | --- | --- |
| [Validate OAuth Token](actions/validate-oauth-token.md) | GET |  |

### Peep

| Action | Method | Description |
| --- | --- | --- |
| [Get Peep](actions/get-peep.md) | GET |  |
| [Invite User to Vybit](actions/invite-user-to-vybit.md) | POST |  |
| [List All Peeps](actions/list-all-peeps.md) | GET |  |
| [List Peeps for Vybit](actions/list-peeps-for-vybit.md) | GET |  |
| [Remove Peep](actions/remove-peep.md) | DELETE |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET |  |

### Public Vybit

| Action | Method | Description |
| --- | --- | --- |
| [Get Public Vybit by Subscription Key](actions/get-public-vybit-by-subscription-key.md) | GET |  |
| [List Public Vybits](actions/list-public-vybits.md) | GET |  |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | POST |  |
| [Delete Reminder](actions/delete-reminder.md) | DELETE |  |
| [List Reminders](actions/list-reminders.md) | GET |  |
| [Update Reminder](actions/update-reminder.md) | PUT |  |

### Sound

| Action | Method | Description |
| --- | --- | --- |
| [Get Sound Details](actions/get-sound-details.md) | GET |  |
| [Search Sounds](actions/search-sounds.md) | GET |  |

### Sound Stream

| Action | Method | Description |
| --- | --- | --- |
| [Play Sound](actions/play-sound.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get API Status](actions/get-api-status.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Following](actions/get-subscription-following.md) | GET |  |
| [List Vybit Subscriptions](actions/list-vybit-subscriptions.md) | GET |  |
| [Send Notification to Group](actions/send-notification-to-group.md) | POST |  |
| [Send Notification to Owner](actions/send-notification-to-owner.md) | POST |  |
| [Subscribe to Vybit](actions/subscribe-to-vybit.md) | POST |  |
| [Unsubscribe from Vybit](actions/unsubscribe-from-vybit.md) | DELETE |  |
| [Update Subscription Following](actions/update-subscription-following.md) | PUT |  |

### Usage Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Metrics](actions/get-usage-metrics.md) | GET |  |

### Vybit

| Action | Method | Description |
| --- | --- | --- |
| [Create Vybit](actions/create-vybit.md) | POST |  |
| [Delete Vybit](actions/delete-vybit.md) | DELETE |  |
| [Get Vybit](actions/get-vybit.md) | GET |  |
| [List Vybits](actions/list-vybits.md) | GET |  |
| [Trigger Vybit Notification](actions/trigger-vybit-notification.md) | POST |  |
| [Update Vybit](actions/update-vybit.md) | PUT |  |

