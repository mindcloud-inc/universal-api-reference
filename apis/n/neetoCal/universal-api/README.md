# <img src="https://images.mindcloud.co/apps/icons/4b2b00a7-6ae1-4e99-a5a9-8f84a88d56ae-2_1777052010515.png" alt="NeetoCal logo" width="28" height="28"> NeetoCal: Universal API

Manage scheduling links, bookings, availabilities, and team members

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neetoCal/latest
- **Category:** Productivity / Scheduling
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://neetocal.com
- **Vendor API docs:** https://apidocs.neetocal.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bookings](actions/list-bookings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Available Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Available Slots](actions/list-available-slots.md) | GET | Finds available slots in NeetoCal for a scheduling link. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Finds bookings in NeetoCal by filter criteria. |

### Meeting Duration

| Action | Method | Description |
| --- | --- | --- |
| [Create Duration](actions/create-meeting-duration.md) | POST | Creates a new meeting duration in NeetoCal. |
| [Delete Duration](actions/delete-meeting-duration.md) | DELETE | Deletes an existing meeting duration from NeetoCal. |
| [Get Duration](actions/get-meeting-duration.md) | GET | Retrieves a meeting duration from NeetoCal. |
| [List Durations for a Meeting](actions/list-meeting-durations.md) | GET | Retrieves meeting durations from NeetoCal for a scheduling link. |
| [Update Duration](actions/update-meeting-duration.md) | PUT | Updates an existing meeting duration in NeetoCal. |

### Meeting Place

| Action | Method | Description |
| --- | --- | --- |
| [Create Place](actions/create-meeting-place.md) | POST | Creates a new meeting place in NeetoCal. |
| [Delete Place](actions/delete-meeting-place.md) | DELETE | Deletes an existing meeting place from NeetoCal. |
| [Get Place](actions/get-meeting-place.md) | GET | Retrieves a meeting place from NeetoCal. |
| [List Places for a Meeting](actions/list-meeting-places.md) | GET | Retrieves meeting places from NeetoCal for a scheduling link. |
| [Update Place](actions/update-meeting-place.md) | PUT | Updates an existing meeting place in NeetoCal. |

### One-time Scheduling Link

| Action | Method | Description |
| --- | --- | --- |
| [Create One-Time Scheduling Link](actions/create-one-time-scheduling-link.md) | POST | Creates a one-time scheduling link in NeetoCal. |

### Scheduling Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduling Link](actions/create-scheduling-link.md) | POST | Creates a new scheduling link in NeetoCal. |
| [Delete Scheduling Link](actions/delete-scheduling-link.md) | DELETE | Deletes an existing scheduling link from NeetoCal. |
| [Get Scheduling Link](actions/get-scheduling-link.md) | GET | Retrieves a scheduling link from NeetoCal. |
| [List Scheduling Links](actions/list-scheduling-links.md) | GET | Finds scheduling links in NeetoCal by filter criteria. |
| [Update Scheduling Link](actions/update-scheduling-link.md) | PUT | Updates an existing scheduling link in NeetoCal. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Member](actions/get-team-member.md) | GET | Retrieves a team member from NeetoCal. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from NeetoCal. |

