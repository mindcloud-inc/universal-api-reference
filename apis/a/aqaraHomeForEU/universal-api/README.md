# <img src="https://images.mindcloud.co/apps/icons/aqara-home-for-us-1776374851211_1776430634956.png" alt="Aqara Home for EU logo" width="28" height="28"> Aqara Home for EU: Universal API

Aqara Home EU app wrapper for Aqara account authorization and the Aqara open API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aqaraHomeForEU/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eu.aqara.com/en-eu
- **Vendor API docs:** https://opendoc.aqara.cn/en/docs/developmanual/apiDocument.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Device Info](actions/query-device-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/query-device-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Token](actions/config-auth-get-token.md) | POST |  |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/config-auth-create-account.md) | POST |  |

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get IFTTT Actions](actions/query-ifttt-action.md) | GET |  |

### Authorization Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Code](actions/config-auth-get-auth-code.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Rename Device](actions/config-device-name.md) | PUT |  |
| [Check Device Bind Status](actions/query-device-bind.md) | GET |  |
| [Get Device Bind Key](actions/query-device-bind-key.md) | GET |  |
| [Get Device Info](actions/query-device-info.md) | GET |  |
| [Get Sub-Device Info](actions/query-device-sub-info.md) | GET |  |
| [Disable Hub Subdevice Mode](actions/write-device-close-connect.md) | PUT |  |
| [Enable Hub Subdevice Mode](actions/write-device-open-connect.md) | PUT |  |
| [Unbind Device](actions/write-device-unbind.md) | DELETE |  |

### Linkage

| Action | Method | Description |
| --- | --- | --- |
| [Create Linkage](actions/config-linkage-create.md) | POST |  |
| [Delete Linkage](actions/config-linkage-delete.md) | DELETE |  |
| [Enable Linkage](actions/config-linkage-enable.md) | PUT |  |
| [Update Linkage](actions/config-linkage-update.md) | PUT |  |
| [Get Linkage Details](actions/query-linkage-detail.md) | GET |  |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [Set Device Position](actions/config-device-position.md) | PUT |  |

### Refresh Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Refresh Token](actions/config-auth-refresh-token.md) | PUT |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Update Resource Info](actions/config-resource-info.md) | PUT |  |
| [Subscribe Resource](actions/config-resource-subscribe.md) | POST |  |
| [Unsubscribe Resource](actions/config-resource-unsubscribe.md) | DELETE |  |
| [Get Resource History](actions/fetch-resource-history.md) | GET |  |
| [Get Resource Statistics](actions/fetch-resource-statistics.md) | GET |  |
| [Get Resource Info](actions/query-resource-info.md) | GET |  |
| [Get Resource Name](actions/query-resource-name.md) | GET |  |
| [Get Resource Value](actions/query-resource-value.md) | GET |  |
| [Control Device Resource](actions/write-resource-device.md) | PUT |  |

### Scene

| Action | Method | Description |
| --- | --- | --- |
| [Create Scene](actions/config-scene-create.md) | POST |  |

### Triggers

| Action | Method | Description |
| --- | --- | --- |
| [Get IFTTT Triggers](actions/query-ifttt-trigger.md) | GET |  |

