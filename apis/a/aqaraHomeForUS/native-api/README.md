# Aqara Home for US: Native API Reference

A consolidated summary of Aqara Home for US's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html
- **API base URL:** `https://open-usa.aqara.com/v3.0/open/api`

## Authentication

### Aqara Project Authorization

Aqara signed headers plus project authorization access token.

### Credentials

- **Access Token:** `accessToken` · optional · Project authorization access token.

[Official authentication documentation](https://opendoc.aqara.com/en/docs/developmanual/authManagement/projectauthMode.html)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Device Binding](actions/check-device-binding.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/addDeviceinterface.html) |
| [Control Resource Device](actions/control-resource-device.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Create Linkage](actions/create-linkage.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/LinkageManagement.html) |
| [Create Position](actions/create-position.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Delete Position](actions/delete-position.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Disable Hub Add-Device Mode](actions/disable-hub-add-device-mode.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/addDeviceinterface.html) |
| [Enable Hub Add-Device Mode](actions/enable-hub-add-device-mode.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/addDeviceinterface.html) |
| [Get Device Bind Key](actions/get-device-bind-key.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/addDeviceinterface.html) |
| [Get Device Info](actions/get-device-info.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Get Device Sub-Info](actions/get-device-sub-info.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Get Position Details](actions/get-position-details.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Get Resource History](actions/get-resource-history.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Info](actions/get-resource-info.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Names](actions/get-resource-names.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Statistics](actions/get-resource-statistics.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Value](actions/get-resource-value.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [List IFTTT Actions](actions/list-ifttt-actions.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/Linkageconfiguration.html) |
| [List IFTTT Triggers](actions/list-ifttt-triggers.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/Linkageconfiguration.html) |
| [List Positions](actions/list-positions.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [List Scenes by Position](actions/list-scenes-by-position.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/SceneManagement.html) |
| [List Supported Gateways](actions/list-supported-gateways.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/addDeviceinterface.html) |
| [Query Firmware Versions](actions/query-firmware-versions.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/FirmwareManagement.html) |
| [Set Device Name](actions/set-device-name.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Set Device Position](actions/set-device-position.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Set Position Time Zone](actions/set-position-time-zone.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Set Resource Info](actions/set-resource-info.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Subscribe Resource Reports](actions/subscribe-resource-reports.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/messagePush/messagePushAPI.html) |
| [Unbind Device](actions/unbind-device.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Unsubscribe Resource Reports](actions/unsubscribe-resource-reports.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/messagePush/messagePushAPI.html) |
| [Update Position](actions/update-position.md) | `POST /` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
