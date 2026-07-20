# <img src="https://images.mindcloud.co/apps/icons/revel-digital_1775223457955.png" alt="Revel Digital logo" width="28" height="28"> Revel Digital: Universal API

Revel Digital is a digital signage and media distribution platform with REST API access for account, devices, content, scheduling, alerts, reporting, and data tables.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/revelDigital/latest
- **Category:** Website & App Building / CMS
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.reveldigital.com
- **Vendor API docs:** https://developer.reveldigital.com/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Send Commands to Multiple Devices](actions/send-commands-to-multiple-devices.md) | POST |  |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert](actions/get-alert.md) | GET |  |
| [List Alerts](actions/list-alerts.md) | GET |  |
| [Update Alert](actions/update-alert.md) | PUT |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Item](actions/get-media-item.md) | GET |  |
| [List Media](actions/list-media.md) | GET |  |
| [Update Media Item](actions/update-media-item.md) | PUT |  |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit Event](actions/get-audit-event.md) | GET |  |
| [List Audit Events](actions/list-audit-events.md) | GET |  |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Table](actions/create-data-table.md) | POST |  |
| [Get Data Table](actions/get-data-table.md) | GET |  |
| [List Data Tables](actions/list-data-tables.md) | GET |  |
| [Update Data Table](actions/update-data-table.md) | PUT |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get Device](actions/get-device.md) | GET |  |
| [List Devices](actions/list-devices.md) | GET |  |
| [Update Device](actions/update-device.md) | PUT |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Device Groups](actions/list-device-groups.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Table Row](actions/create-data-table-row.md) | POST |  |
| [Delete Data Table Row](actions/delete-data-table-row.md) | DELETE |  |
| [Get Data Table Row](actions/get-data-table-row.md) | GET |  |
| [List Data Table Rows](actions/list-data-table-rows.md) | GET |  |
| [Update Data Table Row](actions/update-data-table-row.md) | PUT |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Playlist](actions/get-playlist.md) | GET |  |
| [List Playlists](actions/list-playlists.md) | GET |  |
| [Replace Playlist](actions/replace-playlist.md) | PUT |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule](actions/get-schedule.md) | GET |  |
| [List Schedules](actions/list-schedules.md) | GET |  |

