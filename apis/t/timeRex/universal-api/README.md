# <img src="https://images.mindcloud.co/apps/icons/time-rex_1773773373958.png" alt="TimeRex logo" width="28" height="28"> TimeRex: Universal API

Automate scheduling, sync calendars, and manage bookings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timeRex/latest
- **Category:** Productivity / Scheduling
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timerex.net/
- **Vendor API docs:** https://developers.timerex.net/api/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Calendar](actions/get-calendar.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-calendar?connectionId=$CONNECTION_ID&calendarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar by ID from TimeRex. |
| [List Team Calendars](actions/list-team-calendars.md) | GET | Retrieves calendars in a team from TimeRex. |

### One Time Url

| Action | Method | Description |
| --- | --- | --- |
| [Get One Time URL](actions/get-one-time-url.md) | GET | Retrieves a one-time URL from TimeRex. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team by ID from TimeRex. |
| [Get User Primary Team](actions/get-user-primary-team.md) | GET | Retrieves the current user's primary team from TimeRex. |
| [List User Teams](actions/list-user-teams.md) | GET | Retrieves the current user's teams from TimeRex. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves the current user information from TimeRex. |

