# <img src="https://images.mindcloud.co/apps/icons/id-eq-m-rl-ln-logos_1774299523539.png" alt="Ship24 logo" width="28" height="28"> Ship24: Universal API

Track shipments, search tracking results, manage trackers, and inspect supported couriers with Ship24's Tracking API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ship24/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ship24.com
- **Vendor API docs:** https://docs.ship24.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Couriers](actions/list-couriers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-couriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Courier

| Action | Method | Description |
| --- | --- | --- |
| [List Couriers](actions/list-couriers.md) | GET | Retrieves all available couriers from Ship24. |

### Tracker

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Trackers](actions/bulk-create-trackers.md) | POST | Creates multiple new trackers in Ship24. |
| [Create Tracker](actions/create-tracker.md) | POST | Creates a new tracker in Ship24. |
| [Get Tracker By Client Tracker ID](actions/get-tracker-by-client-tracker-id.md) | GET | Retrieves a tracker by client tracker ID from Ship24. |
| [Get Tracker By Tracker ID](actions/get-tracker-by-tracker-id.md) | GET | Retrieves a tracker by tracker ID from Ship24. |
| [List Trackers](actions/list-trackers.md) | GET | Retrieves existing shipment trackers from Ship24. |
| [Update Tracker](actions/update-tracker.md) | PUT | Updates an existing tracker in Ship24. |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracker And Get Results](actions/create-tracker-and-get-results.md) | POST | Creates a tracker and retrieves tracking results in Ship24. |

### Tracking Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracker Results By Client Tracker ID](actions/get-tracker-results-by-client-tracker-id.md) | GET | Retrieves tracking results by client tracker ID in Ship24. |
| [Get Tracker Results By Tracker ID](actions/get-tracker-results-by-tracker-id.md) | GET | Retrieves tracking results for a Ship24 tracker ID. |
| [Get Tracker Results By Tracking Number](actions/get-tracker-results-by-tracking-number.md) | GET | Retrieves tracker results by tracking number in Ship24. |
| [Get Tracking Results by Tracking Number](actions/get-tracking-results-by-tracking-number.md) | GET | Retrieves tracking results by tracking number from Ship24. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [Resend Tracker Webhook Events](actions/resend-tracker-webhook-events.md) | POST | Resends webhook events for an existing Ship24 tracker. |

