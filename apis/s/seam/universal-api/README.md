# <img src="https://images.mindcloud.co/apps/icons/seam_1774551103220.png" alt="Seam logo" width="28" height="28"> Seam: Universal API

Universal API for smart locks, access systems, thermostats, noise sensors, and related access-control workflows through Seam.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seam/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.seam.co/
- **Vendor API docs:** https://docs.seam.co/latest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace](actions/get-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Connect Webview

| Action | Method | Description |
| --- | --- | --- |
| [Create Connect Webview](actions/create-connect-webview.md) | POST | Creates a new connect webview in Seam. |
| [Get Connect Webview](actions/get-connect-webview.md) | GET | Retrieves a connect webview from Seam. |
| [List Connect Webviews](actions/list-connect-webviews.md) | GET | Retrieves a list of connect webviews from Seam. |

### Connected Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Connected Account](actions/get-connected-account.md) | GET | Retrieves a connected account from Seam. |
| [List Connected Accounts](actions/list-connected-accounts.md) | GET | Retrieves a list of connected accounts from Seam. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get Device](actions/get-device.md) | GET | Retrieves a device from Seam by ID or name. |
| [List Devices](actions/list-devices.md) | GET | Retrieves a list of devices from Seam. |

### Device Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Device Providers](actions/list-device-providers.md) | GET | Retrieves a list of device providers from Seam. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Seam. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from Seam. |

### Lock

| Action | Method | Description |
| --- | --- | --- |
| [Get Lock](actions/get-lock.md) | GET | Retrieves a lock from Seam. |
| [List Locks](actions/list-locks.md) | GET | Retrieves a list of locks from Seam. |

### Noise Sensor

| Action | Method | Description |
| --- | --- | --- |
| [List Noise Sensors](actions/list-noise-sensors.md) | GET | Retrieves a list of noise sensors from Seam. |

### Phone

| Action | Method | Description |
| --- | --- | --- |
| [List Phones](actions/list-phones.md) | GET | Retrieves a list of phones from Seam. |

### Thermostat

| Action | Method | Description |
| --- | --- | --- |
| [Get Thermostat](actions/get-thermostat.md) | GET |  |
| [List Thermostats](actions/list-thermostats.md) | GET | Retrieves a list of thermostats from Seam. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Seam. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Seam. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Seam. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Seam. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Seam. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves the current workspace from Seam. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves a list of workspaces from Seam. |

