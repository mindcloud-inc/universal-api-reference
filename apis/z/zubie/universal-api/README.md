# <img src="https://images.mindcloud.co/apps/icons/zubie_1776366132228.png" alt="Zubie logo" width="28" height="28"> Zubie: Universal API

Access Zubie Zinc fleet telematics data including accounts, devices, events, groups, places, schedules, tags, trips, users, vehicles, media, and visits.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zubie/latest
- **Category:** Support / Field Service
- **Actions:** 49
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zubie.com
- **Vendor API docs:** https://developer.zubie.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Profile](actions/get-current-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (49)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Trip](actions/get-trip.md) | GET | Retrieves a trip from Zubie. |
| [List Trips](actions/list-trips.md) | GET | Retrieves trips from Zubie. |
| [List Vehicle Battery History](actions/list-vehicle-battery-history.md) | GET | Retrieves vehicle battery history from Zubie. |
| [List Visits](actions/list-visits.md) | GET | Retrieves visits from Zubie. |
| [Update Trip](actions/update-trip.md) | PUT | Updates an existing trip in Zubie. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle](actions/create-vehicle.md) | POST | Creates a vehicle in Zubie. |
| [Delete Vehicle](actions/delete-vehicle.md) | DELETE | Deletes a vehicle from Zubie. |
| [Get Vehicle](actions/get-vehicle.md) | GET | Retrieves a vehicle from Zubie. |
| [List Nearby Vehicles](actions/list-nearby-vehicles.md) | GET | Retrieves nearby vehicles from Zubie. |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves vehicles from Zubie. |
| [Update Vehicle](actions/update-vehicle.md) | PUT | Updates an existing vehicle in Zubie. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get Device](actions/get-device.md) | GET | Retrieves a device from Zubie. |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from Zubie. |
| [Update Device](actions/update-device.md) | PUT | Updates an existing device in Zubie. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Zubie. |
| [List Events By Type](actions/list-events-by-type.md) | GET | Retrieves events by type from Zubie. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Media File](actions/fetch-media-file.md) | GET | Retrieves a media file from Zubie. |
| [Get Media Metadata](actions/get-media-metadata.md) | GET | Retrieves media metadata from Zubie. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a group in Zubie. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Zubie. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Zubie. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Zubie. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Deactivate Group](actions/deactivate-group.md) | DELETE | Deactivates a group in Zubie. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in Zubie. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Zubie. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Zubie. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Zubie. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Place](actions/create-place.md) | POST | Creates a place in Zubie. |
| [Delete Place](actions/delete-place.md) | DELETE | Deletes a place from Zubie. |
| [Get Place](actions/get-place.md) | GET | Retrieves a place from Zubie. |
| [Get Trip Points](actions/get-trip-points.md) | GET | Retrieves trip points from Zubie. |
| [List Places](actions/list-places.md) | GET | Retrieves places from Zubie. |
| [Update Place](actions/update-place.md) | PUT | Updates an existing place in Zubie. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Apply Group Memberships](actions/apply-group-memberships.md) | PUT | Applies group memberships in Zubie. |
| [Apply Tag](actions/apply-tag.md) | PUT | Applies a tag in Zubie. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Settings](actions/get-account-settings.md) | GET | Retrieves account settings from Zubie. |
| [Update Account Settings](actions/update-account-settings.md) | PUT | Updates account settings in Zubie. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a schedule in Zubie. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes a schedule from Zubie. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves a schedule from Zubie. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Zubie. |
| [Update Schedule](actions/update-schedule.md) | PUT | Updates an existing schedule in Zubie. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Zubie. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET | Retrieves the current user profile from Zubie. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in Zubie. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Zubie. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Zubie. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Zubie. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Zubie. |

