# <img src="https://images.mindcloud.co/apps/icons/strava_1772574690082.png" alt="Strava logo" width="28" height="28"> Strava: Universal API

Track activities, analyze performance, plan routes, and share workouts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/strava/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.strava.com
- **Vendor API docs:** https://developers.strava.com/docs/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated Athlete](actions/get-authenticated-athlete.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strava/latest/actions/get-authenticated-athlete?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Strava. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Strava by ID. |
| [List Athlete Activities](actions/list-athlete-activities.md) | GET | Retrieves activities for the authenticated athlete from Strava. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in Strava. |

### Athlete

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated Athlete](actions/get-authenticated-athlete.md) | GET | Retrieves the authenticated athlete profile from Strava. |
| [List Activity Kudoers](actions/list-activity-kudoers.md) | GET | Retrieves kudoers for a Strava activity. |

### Athletestats

| Action | Method | Description |
| --- | --- | --- |
| [Get Athlete Stats](actions/get-athlete-stats.md) | GET | Retrieves athlete statistics for a Strava athlete. |

### Club

| Action | Method | Description |
| --- | --- | --- |
| [List Athlete Clubs](actions/list-athlete-clubs.md) | GET | Retrieves clubs for the authenticated athlete from Strava. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Comments](actions/list-activity-comments.md) | GET | Retrieves comments for a Strava activity. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Get Route](actions/get-route.md) | GET | Retrieves a route from Strava by ID. |
| [List Athlete Routes](actions/list-athlete-routes.md) | GET | Retrieves routes for a Strava athlete. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Strava by ID. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Upload](actions/get-upload.md) | GET | Retrieves an activity upload from Strava. |
| [Upload Activity](actions/upload-activity.md) | POST | Creates a new activity upload in Strava. |

### Zones

| Action | Method | Description |
| --- | --- | --- |
| [Get Athlete Zones](actions/get-athlete-zones.md) | GET | Retrieves the authenticated athlete zones from Strava. |

