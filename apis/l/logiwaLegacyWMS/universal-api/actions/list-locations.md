# Logiwa Legacy WMS: List Locations



```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-locations?${params}`, {
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
| `columnCode` | string | no |  |
| `isLocked` | boolean | no |  |
| `lastCountedBeforeDate` | string | no |  |
| `lastModifiedDateEnd` | string | no |  |
| `lastModifiedDateStart` | string | no |  |
| `levelCode` | string | no |  |
| `locationGroupDescription` | string | no |  |
| `locationZoneDescription` | string | no |  |
| `mobileLocationUnitDescription` | string | no |  |
| `pickingTypeDescription` | string | no |  |
| `pickingZoneDescription` | string | no |  |
| `putAwayZoneDescription` | string | no |  |
| `sector` | string | no |  |
| `sectorCode` | string | no |  |
| `storageSystemDescription` | string | no |  |
| `warehouseID` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/LocationSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

