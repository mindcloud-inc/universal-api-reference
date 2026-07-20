# Zubie: Native API Reference

A consolidated summary of Zubie's API configuration and 49 documented operations, with links to official documentation.

- **Official docs:** https://developer.zubie.com/
- **API base URL:** `https://api.zubiecar.com/api/v2/zinc`

## Authentication

### OAuth2

Connect a Zubie Zinc account using OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.zubiecar.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.zubiecar.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account.read account_activity.read places.read user.read vehicles.read`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.zubiecar.com/oauth/token.

[Official authentication documentation](https://developer.zubie.com/overview/authentication)

## Pagination

Use `size` in the query string to set the page size (default 100; accepted range 1–200). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (49 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Group Memberships](actions/apply-group-memberships.md) | `POST /groups/apply` | [docs](https://developer.zubie.com/reference/groups) |
| [Apply Tag](actions/apply-tag.md) | `POST /tag/{tag_key}/apply` | [docs](https://developer.zubie.com/reference/tags) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developer.zubie.com/reference/groups) |
| [Create Place](actions/create-place.md) | `POST /places` | [docs](https://developer.zubie.com/reference/places) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://developer.zubie.com/reference/schedules) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developer.zubie.com/reference/tags) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developer.zubie.com/reference/users) |
| [Create Vehicle](actions/create-vehicle.md) | `POST /vehicles` | [docs](https://developer.zubie.com/reference/vehicles) |
| [Deactivate Group](actions/deactivate-group.md) | `DELETE /group/{group_key}` | [docs](https://developer.zubie.com/reference/groups) |
| [Delete Place](actions/delete-place.md) | `DELETE /place/{place_key}` | [docs](https://developer.zubie.com/reference/places) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedule/{schedule_key}` | [docs](https://developer.zubie.com/reference/schedules) |
| [Delete User](actions/delete-user.md) | `DELETE /user/{user_key}` | [docs](https://developer.zubie.com/reference/users) |
| [Delete Vehicle](actions/delete-vehicle.md) | `DELETE /vehicle/{vehicle_key}` | [docs](https://developer.zubie.com/reference/vehicles) |
| [Fetch Media File](actions/fetch-media-file.md) | `GET /media/{media_key}/fetch` | [docs](https://developer.zubie.com/reference/media) |
| [Get Account Settings](actions/get-account-settings.md) | `GET /account` | [docs](https://developer.zubie.com/reference/account) |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /user` | [docs](https://developer.zubie.com/reference/users) |
| [Get Device](actions/get-device.md) | `GET /device/{key}` | [docs](https://developer.zubie.com/reference/devices) |
| [Get Event](actions/get-event.md) | `GET /event/{event_key}` | [docs](https://developer.zubie.com/reference/events) |
| [Get Group](actions/get-group.md) | `GET /group/{group_key}` | [docs](https://developer.zubie.com/reference/groups) |
| [Get Media Metadata](actions/get-media-metadata.md) | `GET /media/{media_key}` | [docs](https://developer.zubie.com/reference/media) |
| [Get Place](actions/get-place.md) | `GET /place/{place_key}` | [docs](https://developer.zubie.com/reference/places) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedule/{schedule_key}` | [docs](https://developer.zubie.com/reference/schedules) |
| [Get Tag](actions/get-tag.md) | `GET /tag/{tag_key}` | [docs](https://developer.zubie.com/reference/tags) |
| [Get Trip](actions/get-trip.md) | `GET /trip/{trip_key}` | [docs](https://developer.zubie.com/reference/trips) |
| [Get Trip Points](actions/get-trip-points.md) | `GET /trip/{trip_key}/points` | [docs](https://developer.zubie.com/reference/trips) |
| [Get User](actions/get-user.md) | `GET /user/{user_key}` | [docs](https://developer.zubie.com/reference/users) |
| [Get Vehicle](actions/get-vehicle.md) | `GET /vehicle/{vehicle_key}` | [docs](https://developer.zubie.com/reference/vehicles) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://developer.zubie.com/reference/devices) |
| [List Events By Type](actions/list-events-by-type.md) | `GET /events` | [docs](https://developer.zubie.com/reference/events) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developer.zubie.com/reference/groups) |
| [List Nearby Vehicles](actions/list-nearby-vehicles.md) | `GET /vehicles/nearby` | [docs](https://developer.zubie.com/reference/vehicles) |
| [List Places](actions/list-places.md) | `GET /places` | [docs](https://developer.zubie.com/reference/places) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://developer.zubie.com/reference/schedules) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://developer.zubie.com/reference/account) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developer.zubie.com/reference/tags) |
| [List Trips](actions/list-trips.md) | `GET /trips` | [docs](https://developer.zubie.com/reference/trips) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.zubie.com/reference/users) |
| [List Vehicle Battery History](actions/list-vehicle-battery-history.md) | `GET /vehicle/{vehicle_key}/battery-history` | [docs](https://developer.zubie.com/reference/vehicles) |
| [List Vehicles](actions/list-vehicles.md) | `GET /vehicles` | [docs](https://developer.zubie.com/reference/vehicles) |
| [List Visits](actions/list-visits.md) | `GET /places/visits` | [docs](https://developer.zubie.com/reference/visits) |
| [Update Account Settings](actions/update-account-settings.md) | `POST /account` | [docs](https://developer.zubie.com/reference/account) |
| [Update Device](actions/update-device.md) | `POST /device/{key}` | [docs](https://developer.zubie.com/reference/devices) |
| [Update Group](actions/update-group.md) | `POST /group/{group_key}` | [docs](https://developer.zubie.com/reference/groups) |
| [Update Place](actions/update-place.md) | `POST /place/{place_key}` | [docs](https://developer.zubie.com/reference/places) |
| [Update Schedule](actions/update-schedule.md) | `POST /schedule/{schedule_key}` | [docs](https://developer.zubie.com/reference/schedules) |
| [Update Tag](actions/update-tag.md) | `POST /tag/{tag_key}` | [docs](https://developer.zubie.com/reference/tags) |
| [Update Trip](actions/update-trip.md) | `POST /trip/{trip_key}` | [docs](https://developer.zubie.com/reference/trips) |
| [Update User](actions/update-user.md) | `POST /user/{user_key}` | [docs](https://developer.zubie.com/reference/users) |
| [Update Vehicle](actions/update-vehicle.md) | `POST /vehicle/{vehicle_key}` | [docs](https://developer.zubie.com/reference/vehicles) |
