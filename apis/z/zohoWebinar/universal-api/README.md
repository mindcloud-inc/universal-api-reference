# <img src="https://images.mindcloud.co/apps/icons/unnamed_1775229955398.jpeg" alt="Zoho Webinar logo" width="28" height="28"> Zoho Webinar: Universal API

Manage webinars, registrations, attendees, and engagement reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoWebinar/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webinar.zoho.com/
- **Vendor API docs:** https://www.zoho.com/webinar/api/authentication.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization Details](actions/get-organization-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Attendees Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendees Report](actions/get-attendees-report.md) | GET | Retrieves attendee report entries from Zoho Webinar. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from Zoho Webinar. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves organization and user details from Zoho Webinar. |

### Poll

| Action | Method | Description |
| --- | --- | --- |
| [Create Poll](actions/create-poll.md) | POST | Creates a new webinar poll in Zoho Webinar. |
| [Delete Poll](actions/delete-poll.md) | DELETE | Deletes an existing webinar poll from Zoho Webinar. |
| [List Polls](actions/list-polls.md) | GET | Retrieves webinar polls from Zoho Webinar. |
| [Update Poll](actions/update-poll.md) | PUT | Updates an existing webinar poll in Zoho Webinar. |

### Polls Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Polls Report](actions/get-polls-report.md) | GET | Retrieves poll report entries from Zoho Webinar. |

### Question Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Questions Report](actions/get-questions-report.md) | GET | Retrieves question report entries from Zoho Webinar. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Get Recording](actions/get-recording.md) | GET | Retrieves recording details from Zoho Webinar. |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from Zoho Webinar by session type. |

### Registrant

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Register Webinar](actions/bulk-register-webinar.md) | POST | Creates webinar registrations in Zoho Webinar in bulk. |
| [List Webinar Registrations](actions/list-webinar-registrations.md) | GET | Retrieves webinar registrations from Zoho Webinar. |

### Time Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves time zones from Zoho Webinar. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves user details from Zoho Webinar. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Zoho Webinar. |

### Webinar

| Action | Method | Description |
| --- | --- | --- |
| [Create Webinar](actions/create-webinar.md) | POST | Creates a new webinar in Zoho Webinar. |
| [Delete Webinar](actions/delete-webinar.md) | DELETE | Deletes an existing webinar from Zoho Webinar. |
| [Get Webinar](actions/get-webinar.md) | GET | Retrieves webinar details from Zoho Webinar. |
| [List Webinars](actions/list-webinars.md) | GET | Retrieves webinars from Zoho Webinar by list type. |
| [Update Webinar](actions/update-webinar.md) | PUT | Updates an existing webinar in Zoho Webinar. |

### Webinar Attendee Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Webinar Attendee Report](actions/get-webinar-attendee-report.md) | GET | Retrieves webinar attendee report entries from Zoho Webinar. |

