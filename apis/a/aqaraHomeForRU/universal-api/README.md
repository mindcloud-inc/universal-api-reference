# <img src="https://images.mindcloud.co/apps/icons/aqara_1777386991997.png" alt="Aqara Home for RU logo" width="28" height="28"> Aqara Home for RU: Universal API

Aqara Home smart-home wrapper for RU accounts, devices, linkages, scenes, and resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aqaraHomeForRU/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aqara.com/
- **Vendor API docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Position Info](actions/query-position-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/query-position-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Update Device Name](actions/config-device-name.md) | PUT | Updates a device name in Aqara Home for RU. |
| [Update Device Position](actions/config-device-position.md) | PUT | Updates a device position in Aqara Home for RU. |
| [Query Device Info](actions/query-device-info.md) | GET | Retrieves device details from Aqara Home for RU. |
| [Query Sub-Device Info](actions/query-device-sub-info.md) | GET | Retrieves sub-device details from Aqara Home for RU. |

### Ifttt Action

| Action | Method | Description |
| --- | --- | --- |
| [Query IFTTT Actions](actions/query-ifttt-action.md) | GET | Retrieves supported IFTTT actions from Aqara Home for RU. |

### Ifttt Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Query IFTTT Triggers](actions/query-ifttt-trigger.md) | GET | Retrieves supported IFTTT triggers from Aqara Home for RU. |

### Linkage

| Action | Method | Description |
| --- | --- | --- |
| [Create Linkage](actions/config-linkage-create.md) | POST | Creates a linkage in Aqara Home for RU. |
| [Delete Linkage](actions/config-linkage-delete.md) | DELETE | Deletes a linkage from Aqara Home for RU. |
| [Enable Linkage](actions/config-linkage-enable.md) | PUT | Enables or disables a linkage in Aqara Home for RU. |
| [Update Linkage](actions/config-linkage-update.md) | PUT | Updates a linkage in Aqara Home for RU. |
| [Query Linkage Detail](actions/query-linkage-detail.md) | GET | Retrieves linkage details from Aqara Home for RU. |
| [List Linkages by Position](actions/query-linkage-list-by-position-id.md) | GET | Retrieves linkages by position from Aqara Home for RU. |
| [List Linkages by Subject](actions/query-linkage-list-by-subject-id.md) | GET | Retrieves linkages by subject from Aqara Home for RU. |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [Create Position](actions/config-position-create.md) | POST | Creates a position in Aqara Home for RU. |
| [Delete Position](actions/config-position-delete.md) | DELETE | Deletes a position from Aqara Home for RU. |
| [Update Position Time Zone](actions/config-position-time-zone.md) | PUT | Updates a position time zone in Aqara Home for RU. |
| [Update Position](actions/config-position-update.md) | PUT | Updates a position in Aqara Home for RU. |
| [Query Position Detail](actions/query-position-detail.md) | GET | Retrieves position details from Aqara Home for RU. |
| [Query Position Info](actions/query-position-info.md) | GET | Retrieves child positions from Aqara Home for RU. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Update Resource Info](actions/config-resource-info.md) | PUT | Updates resource information in Aqara Home for RU. |
| [Subscribe Resource](actions/config-resource-subscribe.md) | POST | Subscribes to resource updates in Aqara Home for RU. |
| [Unsubscribe Resource](actions/config-resource-unsubscribe.md) | DELETE | Unsubscribes from resource updates in Aqara Home for RU. |
| [Fetch Resource History](actions/fetch-resource-history.md) | GET | Retrieves resource history from Aqara Home for RU. |
| [Fetch Resource Statistics](actions/fetch-resource-statistics.md) | GET | Retrieves resource statistics from Aqara Home for RU. |
| [Query Resource Info](actions/query-resource-info.md) | GET | Retrieves resource details from Aqara Home for RU. |
| [Query Resource Name](actions/query-resource-name.md) | GET | Retrieves resource names from Aqara Home for RU. |
| [Query Resource Value](actions/query-resource-value.md) | GET | Retrieves resource values from Aqara Home for RU. |

### Scene

| Action | Method | Description |
| --- | --- | --- |
| [Create Scene](actions/config-scene-create.md) | POST | Creates a scene in Aqara Home for RU. |
| [Run Scene](actions/config-scene-run.md) | POST | Runs a scene in Aqara Home for RU. |
| [Update Scene](actions/config-scene-update.md) | PUT | Updates a scene in Aqara Home for RU. |

