# <img src="https://images.mindcloud.co/apps/icons/aqara-home-for-us_1776374851211.png" alt="Aqara Home for US logo" width="28" height="28"> Aqara Home for US: Universal API

Aqara Home for US

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aqaraHomeForUS/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://us.aqara.com/
- **Vendor API docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Positions](actions/list-positions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Create Linkage](actions/create-linkage.md) | POST | Creates a new linkage in Aqara Home for US. |
| [List Scenes by Position](actions/list-scenes-by-position.md) | GET | Retrieves scenes from Aqara Home for US by position. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Check Device Binding](actions/check-device-binding.md) | GET | Retrieves Aqara hub binding status from a bind key. |
| [Disable Hub Add-Device Mode](actions/disable-hub-add-device-mode.md) | PUT | Disables hub add-device mode in Aqara Home for US. |
| [Enable Hub Add-Device Mode](actions/enable-hub-add-device-mode.md) | PUT | Enables hub add-device mode in Aqara Home for US. |
| [Get Device Bind Key](actions/get-device-bind-key.md) | GET | Retrieves a bind key for adding an Aqara hub. |
| [Get Device Info](actions/get-device-info.md) | GET | Retrieves device details from Aqara Home for US. |
| [Get Device Sub-Info](actions/get-device-sub-info.md) | GET | Retrieves Aqara sub-device details for a gateway. |
| [List Supported Gateways](actions/list-supported-gateways.md) | GET | Retrieves gateways that support an Aqara sub-device. |
| [Set Device Name](actions/set-device-name.md) | PUT | Updates a device name in Aqara Home for US. |
| [Set Device Position](actions/set-device-position.md) | PUT | Updates a device position in Aqara Home for US. |
| [Unbind Device](actions/unbind-device.md) | DELETE | Deletes an Aqara device binding from its gateway. |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | POST | Creates a new position in Aqara Home for US. |
| [Delete Position](actions/delete-position.md) | DELETE | Deletes an existing position from Aqara Home for US. |
| [Get Position Details](actions/get-position-details.md) | GET | Retrieves Aqara Home for US position details by ID. |
| [List Positions](actions/list-positions.md) | GET | Retrieves subordinate positions from Aqara Home for US. |
| [Set Position Time Zone](actions/set-position-time-zone.md) | PUT | Updates a top-level position time zone in Aqara Home for US. |
| [Update Position](actions/update-position.md) | PUT | Updates an existing position in Aqara Home for US. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [List IFTTT Actions](actions/list-ifttt-actions.md) | GET | Retrieves IFTTT actions for an Aqara object model. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [Query Firmware Versions](actions/query-firmware-versions.md) | GET | Retrieves firmware versions for an Aqara device model. |

### Resource Allocations

| Action | Method | Description |
| --- | --- | --- |
| [Control Resource Device](actions/control-resource-device.md) | PUT | Updates an Aqara device through resource controls. |
| [Get Resource History](actions/get-resource-history.md) | GET | Retrieves historical resource values from an Aqara device. |
| [Get Resource Info](actions/get-resource-info.md) | GET | Retrieves resource details for an Aqara device. |
| [Get Resource Names](actions/get-resource-names.md) | GET | Retrieves default resource names for an Aqara device. |
| [Get Resource Statistics](actions/get-resource-statistics.md) | GET | Retrieves resource statistics from an Aqara device. |
| [Get Resource Value](actions/get-resource-value.md) | GET | Retrieves current resource values from an Aqara device. |
| [Set Resource Info](actions/set-resource-info.md) | PUT | Updates resource information for an Aqara device. |
| [Subscribe Resource Reports](actions/subscribe-resource-reports.md) | POST | Creates a resource report subscription in Aqara Home for US. |
| [Unsubscribe Resource Reports](actions/unsubscribe-resource-reports.md) | DELETE | Deletes a resource report subscription from Aqara Home for US. |

### Triggers

| Action | Method | Description |
| --- | --- | --- |
| [List IFTTT Triggers](actions/list-ifttt-triggers.md) | GET | Retrieves IFTTT triggers for an Aqara object model. |

