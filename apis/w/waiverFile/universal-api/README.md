# <img src="https://images.mindcloud.co/apps/icons/waiver-file_1774029610631.png" alt="WaiverFile logo" width="28" height="28"> WaiverFile: Universal API

Collect waivers, manage events, and sync WaiverFile data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/waiverFile/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.waiverfile.com
- **Vendor API docs:** https://api.waiverfile.com/swagger/ui/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site Details](actions/get-site-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-site-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Check-in Sample

| Action | Method | Description |
| --- | --- | --- |
| [List Sample New Check-Ins](actions/list-sample-new-check-ins.md) | GET | Retrieves sample new check-ins from WaiverFile. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in WaiverFile. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from WaiverFile. |
| [List Events by Category](actions/list-events-by-category.md) | GET | Retrieves events from WaiverFile by category. |
| [List Events by Date Range](actions/list-events-by-date-range.md) | GET | Retrieves events from WaiverFile by date range. |
| [List Upcoming Events](actions/list-upcoming-events.md) | GET | Retrieves upcoming events from WaiverFile. |
| [List Waivers for Event](actions/list-waivers-for-event.md) | GET | Retrieves waivers for an event from WaiverFile. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in WaiverFile. |
| [Upsert Event](actions/upsert-event.md) | PUT | Creates or updates an event in WaiverFile. |

### Event Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Category](actions/create-event-category.md) | POST | Creates a new event category in WaiverFile. |
| [Delete Event Category](actions/delete-event-category.md) | DELETE | Deletes an existing event category from WaiverFile. |
| [List Event Categories](actions/list-event-categories.md) | GET | Retrieves event categories from WaiverFile. |
| [Update Event Category](actions/update-event-category.md) | PUT | Updates an existing event category in WaiverFile. |

### Event Manager

| Action | Method | Description |
| --- | --- | --- |
| [Invite Event Managers](actions/invite-event-managers.md) | POST | Invites event managers to an event in WaiverFile. |
| [Remove Event Managers](actions/remove-event-managers.md) | DELETE | Removes event managers from an event in WaiverFile. |

### Event Sample

| Action | Method | Description |
| --- | --- | --- |
| [List Sample New Events](actions/list-sample-new-events.md) | GET | Retrieves sample new events from WaiverFile. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Ping Event Service](actions/ping-event-service.md) | GET | Checks whether WaiverFile's event service is live. |
| [Ping Service](actions/ping-service.md) | GET | Checks whether the WaiverFile service is live. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Details](actions/get-site-details.md) | GET | Retrieves site details from WaiverFile. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Edit Check-In Subscription](actions/create-edit-check-in-subscription.md) | POST | Creates an edit check-in subscription in WaiverFile. |
| [Create Edit Event Subscription](actions/create-edit-event-subscription.md) | POST | Creates an edit event subscription in WaiverFile. |
| [Create Edit Waiver Subscription](actions/create-edit-waiver-subscription.md) | POST | Creates an edit waiver subscription in WaiverFile. |
| [Create New Check-In Subscription](actions/create-new-check-in-subscription.md) | POST | Creates a new check-in subscription in WaiverFile. |
| [Create New Event Subscription](actions/create-new-event-subscription.md) | POST | Creates a new event subscription in WaiverFile. |
| [Create New Waiver Subscription](actions/create-new-waiver-subscription.md) | POST | Creates a new waiver subscription in WaiverFile. |
| [Delete Edit Check-In Subscription](actions/delete-edit-check-in-subscription.md) | DELETE | Deletes an edit check-in subscription from WaiverFile. |
| [Delete Edit Event Subscription](actions/delete-edit-event-subscription.md) | DELETE | Deletes an edit event subscription from WaiverFile. |
| [Delete Edit Waiver Subscription](actions/delete-edit-waiver-subscription.md) | DELETE | Deletes an edit waiver subscription from WaiverFile. |
| [Delete New Check-In Subscription](actions/delete-new-check-in-subscription.md) | DELETE | Deletes a new check-in subscription from WaiverFile. |
| [Delete New Event Subscription](actions/delete-new-event-subscription.md) | DELETE | Deletes a new event subscription from WaiverFile. |
| [Delete New Waiver Subscription](actions/delete-new-waiver-subscription.md) | DELETE | Deletes a new waiver subscription from WaiverFile. |
| [List Opted-Out SMS Subscribers by Date](actions/list-opted-out-sms-subscribers-by-date.md) | GET | Retrieves opted-out SMS subscribers from WaiverFile by opt-out date. |
| [List SMS Subscribers by Date](actions/list-sms-subscribers-by-date.md) | GET | Retrieves SMS subscribers from WaiverFile by opt-in date. |

### Waiver

| Action | Method | Description |
| --- | --- | --- |
| [Get Waiver](actions/get-waiver.md) | GET | Retrieves a waiver from WaiverFile. |
| [Get Waiver Data Count](actions/get-waiver-data-count.md) | GET | Retrieves waiver data count from WaiverFile. |
| [Get Waiver Page Count by Date Range](actions/get-waiver-page-count-by-date-range.md) | GET | Retrieves waiver page count from WaiverFile by date range. |
| [Get Waiver PDF](actions/get-waiver-pdf.md) | GET | Retrieves a waiver PDF from WaiverFile. |
| [Get Waivers by Reference ID](actions/get-waivers-by-reference-id.md) | GET | Finds waivers in WaiverFile by reference ID. |
| [List Waiver Data](actions/list-waiver-data.md) | GET | Retrieves waiver data from WaiverFile. |
| [List Waivers by Date Range](actions/list-waivers-by-date-range.md) | GET | Retrieves waivers from WaiverFile by date range. |
| [Search Waivers](actions/search-waivers.md) | GET | Finds waivers in WaiverFile. |

### Waiver Form

| Action | Method | Description |
| --- | --- | --- |
| [List Active Waiver Forms](actions/list-active-waiver-forms.md) | GET | Retrieves active waiver forms from WaiverFile. |
| [List All Waiver Forms](actions/list-all-waiver-forms.md) | GET | Retrieves all waiver forms from WaiverFile. |

### Waiver Sample

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Edited Waivers](actions/list-sample-edited-waivers.md) | GET | Retrieves sample edited waivers from WaiverFile. |
| [List Sample New Waivers](actions/list-sample-new-waivers.md) | GET | Retrieves sample new waivers from WaiverFile. |

