# <img src="https://images.mindcloud.co/apps/icons/simpliroute-icon_1777044551794.png" alt="SimpliRoute logo" width="28" height="28"> SimpliRoute: Universal API

Plan routes, optimize deliveries, manage visits, and track drivers and vehicles with SimpliRoute.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpliRoute/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://simpliroute.com/
- **Vendor API docs:** https://documentation.simpliroute.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves the authenticated account from SimpliRoute. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle](actions/create-vehicle.md) | POST | Creates a new vehicle in SimpliRoute. |
| [Delete Vehicle](actions/delete-vehicle.md) | DELETE | Deletes an existing vehicle from SimpliRoute. |
| [Update Vehicle](actions/update-vehicle.md) | PUT | Updates an existing vehicle in SimpliRoute. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a driver from SimpliRoute by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves drivers from SimpliRoute. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new driver in SimpliRoute. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing driver from SimpliRoute. |
| [Update User](actions/update-user.md) | PUT | Updates an existing driver in SimpliRoute. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle](actions/get-vehicle.md) | GET | Retrieves a vehicle from SimpliRoute by ID. |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves vehicles from SimpliRoute. |

