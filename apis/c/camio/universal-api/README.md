# <img src="https://images.mindcloud.co/apps/icons/camio_1776361587349.png" alt="Camio logo" width="28" height="28"> Camio: Universal API

Monitor cameras, search video, manage settings, and automate alerts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/camio/latest
- **Category:** IT Operations / Observability
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://camio.com
- **Vendor API docs:** https://api.camio.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Connected Cameras](actions/list-connected-cameras.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-connected-cameras?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account from Camio. |
| [List User Accounts](actions/list-user-accounts.md) | GET | Retrieves user accounts from Camio. |

### Camera

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Cameras](actions/list-connected-cameras.md) | GET | Retrieves connected cameras from Camio. |
| [Search Cameras](actions/search-cameras.md) | GET | Finds cameras in Camio by search text. |

### Camio

| Action | Method | Description |
| --- | --- | --- |
| [Create Camio](actions/create-camio.md) | POST | Creates a Camio in Camio. |
| [Delete Camio](actions/delete-camio.md) | DELETE | Deletes a Camio from Camio. |
| [Get Camio](actions/get-camio.md) | GET | Retrieves a Camio from Camio. |
| [List Camios](actions/list-camios.md) | GET | Retrieves Camios from Camio. |
| [Update Camio Collaborators](actions/update-camio-collaborators.md) | PUT | Updates Camio collaborators in Camio. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from Camio. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Search Events](actions/search-events.md) | GET | Finds video events in Camio by search text. |

### Pinned Query

| Action | Method | Description |
| --- | --- | --- |
| [Create Pinned Query](actions/create-pinned-query.md) | POST | Creates a pinned query in Camio. |
| [Delete Pinned Query](actions/delete-pinned-query.md) | DELETE | Deletes a pinned query from Camio. |
| [List Pinned Queries](actions/list-pinned-queries.md) | GET | Retrieves pinned queries from Camio. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a profile from Camio. |
| [Update Profile](actions/update-profile.md) | PUT | Updates a profile in Camio. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings](actions/get-settings.md) | GET | Retrieves settings from Camio. |
| [Update Settings](actions/update-settings.md) | PUT | Updates settings in Camio. |

### Upload Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Upload Token](actions/get-upload-token.md) | GET | Retrieves an upload token from Camio. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves a user from Camio. |

