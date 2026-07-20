# BigDataCloud: Get Time Zone by Location

Retrieves time zone details by location from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-time-zone-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-time-zone-by-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-time-zone-by-location?${params}`, {
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
| `latitude` | number | no | Latitude value in the WGS 84 reference system. Example: `-34.9313`. |
| `longitude` | number | no | Longitude value in the WGS 84 reference system. Example: `138.59669`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `utcReference` | number | no | UTC time reference in Unix time seconds. Example: `1712534400`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "effectiveTimeZoneFull": "string",
      "effectiveTimeZoneShort": "string",
      "ianaTimeId": "string",
      "isDaylightSavingTime": true,
      "localTime": "2026-05-07T12:00:00.000Z",
      "utcOffset": "string",
      "utcOffsetSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `effectiveTimeZoneFull` | string |  |
| `effectiveTimeZoneShort` | string |  |
| `ianaTimeId` | string |  |
| `isDaylightSavingTime` | boolean |  |
| `localTime` | date |  |
| `utcOffset` | string |  |
| `utcOffsetSeconds` | number |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/timezone-by-location` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-zone-by-location.md) for the provider-specific parameters and requirements.

