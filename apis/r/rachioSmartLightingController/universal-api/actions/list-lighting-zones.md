# Rachio Smart Lighting Controller: List Lighting Zones



```
GET https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-lighting-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Lighting Controller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-lighting-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-lighting-zones?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lightingAreaId` | string | no | Limit results to a lighting area. |
| `lightingControllerId` | string | no | Limit results to a lighting controller. |
| `lightingSceneId` | string | no | Limit results to a lighting scene. |
| `lightingZoneGroupId` | string | no | Limit results to a lighting zone group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Lighting Controller API returns.

## Native endpoint

Through the native Rachio Smart Lighting Controller API, this operation is `GET https://cloud-rest.rach.io/lighting/listLightingZones` (base URL `https://cloud-rest.rach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lighting-zones.md) for the provider-specific parameters and requirements.

