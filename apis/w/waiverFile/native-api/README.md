# WaiverFile: Native API Reference

A consolidated summary of WaiverFile's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://api.waiverfile.com/swagger/ui/index
- **OpenAPI specification:** https://api.waiverfile.com/swagger/docs/v1
- **API base URL:** `https://api.waiverfile.com/api/v1`

## Authentication

### API Key

Connect WaiverFile using an API key and Site ID from Settings >> API.

### Credentials

- **API Key:** `apiKey` · required
- **Site ID:** `siteId` · required · Your WaiverFile Site ID from Settings >> API.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.waiverfile.com/Resources/Help/Export-and-Integrations/Integrations/Zapier.aspx)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size. Use `pageIndex` in the query string to choose the page; numbering starts at 1.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Edit Check-In Subscription](actions/create-edit-check-in-subscription.md) | `POST /subscribe/editcheckin` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create Edit Event Subscription](actions/create-edit-event-subscription.md) | `POST /subscribe/editevent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create Edit Waiver Subscription](actions/create-edit-waiver-subscription.md) | `POST /subscribe/editwaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create Event](actions/create-event.md) | `POST /InsertEvent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create Event Category](actions/create-event-category.md) | `POST /InsertEventCategory` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create New Check-In Subscription](actions/create-new-check-in-subscription.md) | `POST /subscribe/newcheckin` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create New Event Subscription](actions/create-new-event-subscription.md) | `POST /subscribe/newevent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Create New Waiver Subscription](actions/create-new-waiver-subscription.md) | `POST /subscribe/newwaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete Edit Check-In Subscription](actions/delete-edit-check-in-subscription.md) | `DELETE /deletesubscribe/editcheckin` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete Edit Event Subscription](actions/delete-edit-event-subscription.md) | `DELETE /deletesubscribe/editevent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete Edit Waiver Subscription](actions/delete-edit-waiver-subscription.md) | `DELETE /deletesubscribe/editwaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete Event](actions/delete-event.md) | `GET /DeleteEvent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete Event Category](actions/delete-event-category.md) | `POST /DeleteEventCategory` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete New Check-In Subscription](actions/delete-new-check-in-subscription.md) | `DELETE /deletesubscribe/newcheckin` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete New Event Subscription](actions/delete-new-event-subscription.md) | `DELETE /deletesubscribe/newevent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Delete New Waiver Subscription](actions/delete-new-waiver-subscription.md) | `DELETE /deletesubscribe/newwaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Get Site Details](actions/get-site-details.md) | `GET /GetSiteDetails` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Get Waiver](actions/get-waiver.md) | `GET /GetWaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Get Waiver Data Count](actions/get-waiver-data-count.md) | `GET /GetWaiverDataCount` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Get Waiver Page Count by Date Range](actions/get-waiver-page-count-by-date-range.md) | `GET /GetAllWaiversByDateRangePageCount` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Get Waiver PDF](actions/get-waiver-pdf.md) | `GET /GetWaiverPDF` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Get Waivers by Reference ID](actions/get-waivers-by-reference-id.md) | `GET /GetWaiversByReferenceID` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Invite Event Managers](actions/invite-event-managers.md) | `POST /InviteEventManagers` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Active Waiver Forms](actions/list-active-waiver-forms.md) | `GET /GetActiveWaiverForms` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List All Waiver Forms](actions/list-all-waiver-forms.md) | `GET /GetAllWaiverForms` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Event Categories](actions/list-event-categories.md) | `GET /GetEventCategories` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Events by Category](actions/list-events-by-category.md) | `GET /GetEventsByCategory` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Events by Date Range](actions/list-events-by-date-range.md) | `GET /GetEventsByDateRange` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Opted-Out SMS Subscribers by Date](actions/list-opted-out-sms-subscribers-by-date.md) | `GET /GetOptedOutSubscribersByOptOutDate` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Sample Edited Waivers](actions/list-sample-edited-waivers.md) | `GET /sampledata/editwaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Sample New Check-Ins](actions/list-sample-new-check-ins.md) | `GET /sampledata/newcheckin` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Sample New Events](actions/list-sample-new-events.md) | `GET /sampledata/newevent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Sample New Waivers](actions/list-sample-new-waivers.md) | `GET /sampledata/newwaiver` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List SMS Subscribers by Date](actions/list-sms-subscribers-by-date.md) | `GET /GetSubscribersByDate` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Upcoming Events](actions/list-upcoming-events.md) | `GET /GetUpcomingEvents` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Waiver Data](actions/list-waiver-data.md) | `GET /GetWaiverData` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Waivers by Date Range](actions/list-waivers-by-date-range.md) | `GET /GetAllWaiversByDateRange` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [List Waivers for Event](actions/list-waivers-for-event.md) | `GET /GetWaiversForEvent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Ping Event Service](actions/ping-event-service.md) | `POST /EvtPing` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Ping Service](actions/ping-service.md) | `GET /Ping` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Remove Event Managers](actions/remove-event-managers.md) | `POST /RemoveEventManagers` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Search Waivers](actions/search-waivers.md) | `GET /SearchWaivers` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Update Event](actions/update-event.md) | `POST /UpdateEvent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Update Event Category](actions/update-event-category.md) | `POST /UpdateEventCategory` | [docs](https://api.waiverfile.com/swagger/ui/index) |
| [Upsert Event](actions/upsert-event.md) | `POST /InsertOrUpdateEvent` | [docs](https://api.waiverfile.com/swagger/ui/index) |
