# <img src="https://images.mindcloud.co/apps/icons/images_1775068378991.jpeg" alt="Channex logo" width="28" height="28"> Channex: Universal API

Manage properties, inventory, rates, bookings, and channel updates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/channex/latest
- **Category:** Commerce / ERP
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://channex.io
- **Vendor API docs:** https://docs.channex.io/api-v.1-documentation/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Properties](actions/list-properties.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | GET | Retrieves room type availability from Channex. |
| [Update Availability](actions/update-availability.md) | PUT | Updates room type availability in Channex. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking Due Invalid Card](actions/cancel-booking-due-invalid-card.md) | PUT | Cancels a booking for an invalid card in Channex. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves an existing booking from Channex. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from your Channex account. |
| [Report Booking Invalid Card](actions/report-booking-invalid-card.md) | PUT | Reports an invalid booking card in Channex. |
| [Report Booking No Show](actions/report-booking-no-show.md) | PUT | Reports a booking no-show in Channex. |

### Booking Revision

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Booking Revision](actions/acknowledge-booking-revision.md) | PUT | Acknowledges a booking revision in Channex. |
| [Get Booking Revision](actions/get-booking-revision.md) | GET | Retrieves a booking revision from Channex. |
| [Get Booking Revision Feed](actions/get-booking-revision-feed.md) | GET | Retrieves the booking revision feed from Channex. |
| [List Booking Revisions](actions/list-booking-revisions.md) | GET | Retrieves booking revisions from your Channex account. |

### Channel Availability Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel Availability Rule](actions/create-channel-availability-rule.md) | POST | Creates a channel availability rule in Channex. |
| [Delete Channel Availability Rule](actions/delete-channel-availability-rule.md) | DELETE | Deletes a channel availability rule from Channex. |
| [Get Channel Availability Rule](actions/get-channel-availability-rule.md) | GET | Retrieves a channel availability rule from Channex. |
| [List Channel Availability Rules](actions/list-channel-availability-rules.md) | GET | Retrieves channel availability rules from Channex. |
| [Update Channel Availability Rule](actions/update-channel-availability-rule.md) | PUT | Updates a channel availability rule in Channex. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST | Creates a new property in Channex. |
| [Get Property](actions/get-property.md) | GET | Retrieves an existing property from Channex. |
| [List Properties](actions/list-properties.md) | GET | Retrieves properties from your Channex account. |
| [List Property Options](actions/list-property-options.md) | GET | Retrieves property options from your Channex account. |
| [Update Property](actions/update-property.md) | PUT | Updates an existing property in Channex. |

### Rate Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Rate Plan](actions/create-rate-plan.md) | POST | Creates a rate plan in Channex. |
| [Delete Rate Plan](actions/delete-rate-plan.md) | DELETE | Deletes a rate plan from Channex. |
| [Get Rate Plan](actions/get-rate-plan.md) | GET | Retrieves a rate plan from Channex. |
| [List Rate Plan Options](actions/list-rate-plan-options.md) | GET | Retrieves rate plan options from Channex. |
| [List Rate Plans](actions/list-rate-plans.md) | GET | Retrieves rate plans from your Channex account. |
| [Update Rate Plan](actions/update-rate-plan.md) | PUT | Updates a rate plan in Channex. |

### Restriction

| Action | Method | Description |
| --- | --- | --- |
| [Get Restrictions](actions/get-restrictions.md) | GET | Retrieves rate plan restrictions from Channex. |
| [Update Restrictions](actions/update-restrictions.md) | PUT | Updates rate plan restrictions in Channex. |

### Room Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Room Type](actions/create-room-type.md) | POST | Creates a room type in Channex. |
| [Delete Room Type](actions/delete-room-type.md) | DELETE | Deletes a room type from Channex. |
| [Get Room Type](actions/get-room-type.md) | GET | Retrieves a room type from Channex. |
| [List Room Type Options](actions/list-room-type-options.md) | GET | Retrieves room type options from Channex. |
| [List Room Types](actions/list-room-types.md) | GET | Retrieves room types from your Channex account. |
| [Update Room Type](actions/update-room-type.md) | PUT | Updates a room type in Channex. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Channex. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Channex. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves an existing webhook from Channex. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Channex account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Channex. |

