# <img src="https://images.mindcloud.co/apps/icons/e-cal_1776700203498.png" alt="ECAL logo" width="28" height="28"> ECAL: Universal API

ECAL provides API access for managing calendars, events, private subscriber events, subscribers, and partner sub-accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eCAL/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ecal.com
- **Vendor API docs:** https://docs.ecal.com/reference/apiv2.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calendars](actions/list-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new sub-account in ECAL. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves sub-accounts from ECAL. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new calendar in ECAL. |
| [Delete Calendar](actions/delete-calendar.md) | DELETE | Deletes an existing calendar from ECAL. |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar from ECAL by ID. |
| [Get Calendar By Reference](actions/get-calendar-by-reference.md) | GET | Retrieves a calendar from ECAL by reference. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from ECAL. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in ECAL. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Events By Reference Type](actions/bulk-update-events-by-reference-type.md) | PUT | Updates ECAL events by reference type. |
| [Create Event](actions/create-event.md) | POST | Creates a new event in ECAL. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an ECAL event by ID or reference. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from ECAL by ID. |
| [List Events](actions/list-events.md) | GET | Retrieves events from ECAL. |
| [Update Event](actions/update-event.md) | PUT | Updates an ECAL event by ID or reference. |

### Private Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Private Events](actions/create-batch-private-events.md) | POST | Creates batch private events in ECAL. |
| [Create Private Event](actions/create-private-event.md) | POST | Creates a private event for an ECAL subscriber. |
| [Delete Batch Private Events](actions/delete-batch-private-events.md) | DELETE | Deletes batch private events from ECAL. |
| [Delete Private Event](actions/delete-private-event.md) | DELETE | Deletes a subscriber's private ECAL event. |
| [List Batch Private Events By Reference Type](actions/list-batch-private-events-by-reference-type.md) | GET | Retrieves batch private events by ECAL reference type. |
| [List Batch Private Events By Subscriber](actions/list-batch-private-events-by-subscriber.md) | GET | Retrieves batch private events for one ECAL subscriber. |
| [List Batch Private Events By Subscriber And Reference Type](actions/list-batch-private-events-by-subscriber-and-reference-type.md) | GET | Retrieves batch private events by subscriber and reference type. |
| [List Private Events](actions/list-private-events.md) | GET | Retrieves a subscriber's private events from ECAL. |
| [Search Batch Private Events By IDs](actions/search-batch-private-events-by-ids.md) | GET | Finds batch private ECAL events by event IDs. |
| [Update Private Event](actions/update-private-event.md) | PUT | Updates a subscriber's private ECAL event. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber By ECAL ID](actions/get-subscriber-by-ecal-id.md) | GET | Retrieves an ECAL subscriber by ECAL ID. |
| [Get Subscriber By Email](actions/get-subscriber-by-email.md) | GET | Retrieves an ECAL subscriber by email address. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | DELETE | Unsubscribes a subscriber from ECAL. |

### Subscriber Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Subscriptions](actions/add-subscriber-subscriptions.md) | PUT | Adds calendar subscriptions to an ECAL subscriber. |
| [Remove Subscriber Subscriptions](actions/remove-subscriber-subscriptions.md) | PUT | Removes calendar subscriptions from an ECAL subscriber. |

