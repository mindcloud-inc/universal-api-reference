# <img src="https://images.mindcloud.co/apps/icons/airzone-cloud-icon_1776362601184.png" alt="Airzone Cloud logo" width="28" height="28"> Airzone Cloud: Universal API

Airzone Cloud Web API wrapper for installations, devices, locations, and user profile operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airzoneCloud/latest
- **Category:** Support / Field Service
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.airzonecloud.com/
- **Vendor API docs:** https://developers.airzonecloud.com/docs/web-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Update Device Parameter](actions/update-device-parameter.md) | PUT | Updates a device parameter in Airzone Cloud. |

### Device Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Configuration](actions/get-device-configuration.md) | GET | Retrieves device configuration from Airzone Cloud. |

### Device Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Status](actions/get-device-status.md) | GET | Retrieves a device's state from Airzone Cloud. |

### Installation

| Action | Method | Description |
| --- | --- | --- |
| [Get Installation](actions/get-installation.md) | GET | Retrieves a user's installation relation from Airzone Cloud. |
| [List Installations](actions/list-installations.md) | GET | Retrieves confirmed user installations from Airzone Cloud. |
| [Update Installation](actions/update-installation.md) | PUT | Updates all climate zones in an installation in Airzone Cloud. |

### Installation Group

| Action | Method | Description |
| --- | --- | --- |
| [Update Installation Group](actions/update-installation-group.md) | PUT | Updates all devices in an installation group in Airzone Cloud. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Installation Location](actions/get-installation-location.md) | GET | Retrieves an installation location from Airzone Cloud. |

### Session Token Pair

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Token Pair](actions/create-session-token-pair.md) | POST | Creates a session token pair in Airzone Cloud. |
| [Refresh Session Token Pair](actions/refresh-session-token-pair.md) | POST | Creates a refreshed session token pair in Airzone Cloud. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user profile from Airzone Cloud. |

### User Session

| Action | Method | Description |
| --- | --- | --- |
| [Logout User](actions/logout-user.md) | DELETE | Deletes the current user session from Airzone Cloud. |

### Webserver Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Webserver Status](actions/get-webserver-status.md) | GET | Retrieves webserver status and config from Airzone Cloud. |

