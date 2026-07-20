# <img src="https://images.mindcloud.co/apps/icons/late_1774377959341.png" alt="Late logo" width="28" height="28"> Late: Universal API

Schedule posts, connect accounts, and manage social conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/late/latest
- **Category:** Marketing / Social Media
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zernio.com
- **Vendor API docs:** https://docs.zernio.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage Stats](actions/get-usage-stats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/get-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Check Accounts Health](actions/check-accounts-health.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |

### Accountgroup

| Action | Method | Description |
| --- | --- | --- |
| [List Account Groups](actions/list-account-groups.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST |  |
| [Delete Post](actions/delete-post.md) | DELETE |  |
| [Get Post](actions/get-post.md) | GET |  |
| [List Posts](actions/list-posts.md) | GET |  |
| [Update Post](actions/update-post.md) | PUT |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST |  |
| [Delete Profile](actions/delete-profile.md) | DELETE |  |
| [Get Profile](actions/get-profile.md) | GET |  |
| [List Profiles](actions/list-profiles.md) | GET |  |
| [Update Profile](actions/update-profile.md) | PUT |  |

### Queueschedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Queue Schedule](actions/create-queue-schedule.md) | POST |  |
| [Delete Queue Schedule](actions/delete-queue-schedule.md) | DELETE |  |
| [Get Next Queue Slot](actions/get-next-queue-slot.md) | GET |  |
| [List Queue Schedules](actions/list-queue-schedules.md) | GET |  |
| [Preview Queue Slots](actions/preview-queue-slots.md) | GET |  |
| [Update Queue Schedule](actions/update-queue-schedule.md) | PUT |  |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Stats](actions/get-usage-stats.md) | GET |  |

