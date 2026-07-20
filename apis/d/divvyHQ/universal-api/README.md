# <img src="https://images.mindcloud.co/apps/icons/divvy-hq_1775150304310.png" alt="DivvyHQ logo" width="28" height="28"> DivvyHQ: Universal API

DivvyHQ is a content planning and production workflow platform for marketing and content teams. This app connects to DivvyHQ's Enterprise Accounts API for calendars, content items, campaigns, production tasks, team members, and related workflow data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/divvyHQ/latest
- **Category:** Marketing
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lytho.com/
- **Vendor API docs:** https://developer.divvyhq.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Allowed Content Type In Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Allowed Content Types In Calendars](actions/list-allowed-content-types-in-calendars.md) | GET |  |
| [Patch Allowed Content Type In Calendar](actions/patch-allowed-content-type-in-calendar.md) | PUT |  |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Entry](actions/get-calendar-entry.md) | GET |  |
| [List Calendar Entries](actions/list-calendar-entries.md) | GET |  |
| [Search Calendar Entries](actions/search-calendar-entries.md) | GET |  |

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [Create Simple Calendar](actions/create-simple-calendar.md) | POST |  |
| [Get Base Calendar](actions/get-base-calendar.md) | GET |  |
| [Get Simple Calendar](actions/get-simple-calendar.md) | GET |  |
| [List Base Calendars](actions/list-base-calendars.md) | GET |  |
| [Patch Simple Calendar](actions/patch-simple-calendar.md) | PUT |  |
| [Update Simple Calendar](actions/update-simple-calendar.md) | PUT |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [Patch Campaign](actions/patch-campaign.md) | PUT |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Content Item](actions/create-content-item.md) | POST |  |
| [Get Content Item](actions/get-content-item.md) | GET |  |
| [List Content Items](actions/list-content-items.md) | GET |  |
| [Patch Content Item](actions/patch-content-item.md) | PUT |  |
| [Update Content Item](actions/update-content-item.md) | PUT |  |

### Parent Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Parent Calendar](actions/get-parent-calendar.md) | GET |  |
| [List Parent Calendars](actions/list-parent-calendars.md) | GET |  |

### Role In Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Role In Calendar](actions/get-role-in-calendar.md) | GET |  |
| [List Roles In Calendars](actions/list-roles-in-calendars.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Production Task](actions/create-production-task.md) | POST |  |
| [Get Production Task](actions/get-production-task.md) | GET |  |
| [List Production Tasks](actions/list-production-tasks.md) | GET |  |
| [Patch Production Task](actions/patch-production-task.md) | PUT |  |
| [Update Production Task](actions/update-production-task.md) | PUT |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Member](actions/get-team-member.md) | GET |  |
| [List Team Members](actions/list-team-members.md) | GET |  |

