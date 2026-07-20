# <img src="https://images.mindcloud.co/apps/icons/aqara-home-for-kr_1776429711479.png" alt="Aqara Home for KR logo" width="28" height="28"> Aqara Home for KR: Universal API

Aqara Open Platform app for the South Korea region.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aqaraHomeForKR/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.aqara.com/register
- **Vendor API docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Devices](actions/list-devices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from Aqara Home for KR. |
| [List Gateway Subdevices](actions/list-gateway-subdevices.md) | GET | Retrieves subdevices for a gateway in Aqara Home for KR. |
| [Rename Device](actions/rename-device.md) | PUT | Updates a device name in Aqara Home for KR. |

### Position

| Action | Method | Description |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | POST | Creates a new position in Aqara Home for KR. |
| [Delete Position](actions/delete-position.md) | DELETE | Deletes an existing position from Aqara Home for KR. |
| [Get Position Details](actions/get-position-details.md) | GET | Retrieves position details from Aqara Home for KR. |
| [List Positions](actions/list-positions.md) | GET | Retrieves subordinate positions in Aqara Home for KR. |
| [Update Position](actions/update-position.md) | PUT | Updates an existing position in Aqara Home for KR. |
| [Update Position Timezone](actions/update-position-timezone.md) | PUT | Updates a top-level position timezone in Aqara Home for KR. |

