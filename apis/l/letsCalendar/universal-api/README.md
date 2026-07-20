# <img src="https://images.mindcloud.co/apps/icons/lets-calendar_1774640610042.png" alt="Let's Calendar logo" width="28" height="28"> Let's Calendar: Universal API

Create, send, and track calendar invite campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/letsCalendar/latest
- **Category:** Marketing
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.letscalendar.com/
- **Vendor API docs:** https://panel.letscalendar.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Senders](actions/list-senders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Attendees](actions/list-campaign-attendees.md) | GET | Retrieves campaign attendees from Let's Calendar. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Let's Calendar. |
| [Get Campaign Details](actions/get-campaign-details.md) | GET | Retrieves campaign details from Let's Calendar. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaign records from Let's Calendar. |
| [Stop Campaign](actions/stop-campaign.md) | PUT | Stops an active campaign in Let's Calendar. |
| [Toggle Campaign Automation Status](actions/toggle-campaign-automation-status.md) | PUT | Updates campaign automation status in Let's Calendar. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Let's Calendar. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Multiple Contacts to Campaign](actions/add-multiple-contacts-to-campaign.md) | POST | Adds multiple contacts to a campaign in Let's Calendar. |
| [Add Single Contact to Campaign](actions/add-single-contact-to-campaign.md) | POST | Adds a contact to a campaign in Let's Calendar. |
| [Export Campaign Contacts](actions/export-campaign-contacts.md) | GET | Exports campaign contacts from Let's Calendar. |
| [Upload Campaign Contacts](actions/upload-campaign-contacts.md) | POST | Uploads campaign contacts to Let's Calendar from CSV or Excel. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled Invites](actions/cancel-scheduled-invites.md) | PUT | Cancels scheduled invites in Let's Calendar. |
| [Schedule Calendar Invites](actions/schedule-calendar-invites.md) | POST | Schedules calendar invites in Let's Calendar. |
| [Send Calendar Invites](actions/send-calendar-invites.md) | POST | Sends calendar invites to attendees in Let's Calendar. |
| [Update Campaign Invites](actions/update-campaign-invites.md) | PUT | Updates and sends calendar invites in Let's Calendar. |

### Sender Email

| Action | Method | Description |
| --- | --- | --- |
| [List Senders](actions/list-senders.md) | GET | Retrieves sender emails from Let's Calendar. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List Timezones](actions/list-timezones.md) | GET | Retrieves available timezones from Let's Calendar. |

