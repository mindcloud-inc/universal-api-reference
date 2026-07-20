# <img src="https://images.mindcloud.co/apps/icons/zoho-meeting_1773940914210.png" alt="Zoho Meeting logo" width="28" height="28"> Zoho Meeting: Universal API

Zoho Meeting is Zoho's meetings and webinars platform. This wrapper covers Zoho Meeting's OAuth 2.0 API for managing organization context, license details, meetings, and webinars.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoMeeting/latest
- **Category:** Communication / Video Communications
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/meeting/
- **Vendor API docs:** https://www.zoho.com/meeting/api-integration.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Details](actions/get-current-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-current-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [Create Webinar Registrations](actions/create-webinar-registrations.md) | POST | Creates webinar registrations in bulk in Zoho Meeting. |
| [List Webinar Registrations](actions/list-webinar-registrations.md) | GET | Retrieves webinar registrations from Zoho Meeting. |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | POST | Creates a new meeting in Zoho Meeting. |
| [Delete Meeting](actions/delete-meeting.md) | DELETE | Deletes an existing meeting from Zoho Meeting. |
| [Get Meeting Details](actions/get-meeting-details.md) | GET | Retrieves meeting details from Zoho Meeting. |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings from Zoho Meeting. |
| [Update Meeting](actions/update-meeting.md) | PUT | Updates an existing meeting in Zoho Meeting. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Current License Details](actions/get-current-license-details.md) | GET | Retrieves current license details from Zoho Meeting. |
| [Get Current User Details](actions/get-current-user-details.md) | GET | Retrieves current user details from Zoho Meeting. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Webinar](actions/create-webinar.md) | POST | Creates a new webinar in Zoho Meeting. |
| [Delete Webinar](actions/delete-webinar.md) | DELETE | Deletes an existing webinar from Zoho Meeting. |
| [Get Webinar Details](actions/get-webinar-details.md) | GET | Retrieves webinar details from Zoho Meeting. |
| [List Webinars](actions/list-webinars.md) | GET | Retrieves webinars from Zoho Meeting. |
| [Update Webinar](actions/update-webinar.md) | PUT | Updates an existing webinar in Zoho Meeting. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves user details from Zoho Meeting. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Zoho Meeting. |

