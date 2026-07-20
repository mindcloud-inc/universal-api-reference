# Federal Communications Commission: Get Broadcast Contour

Retrieves FCC broadcast contour data by service and identifier.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-broadcast-contour
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-broadcast-contour?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-broadcast-contour?${params}`, {
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
| `format` | string | no | Response format. FCC documents json, jsonp, shp, kml, gml, csv. Use json for normal API runs. |
| `idType` | string | no | Identifier type. Valid values include facilityid, callsign, filenumber, applicationid, antennaid. |
| `idValue` | string | no | Identifier value for the selected ID type. |
| `serviceType` | string | no | Contour service type. Valid values documented by FCC: tv, fm, am. |
| `stationClass` | string | no | AM-only station class; ignored for TV and FM. |
| `timePeriod` | string | no | AM-only time period; FCC currently documents day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<object> | Contour GeoJSON features. |
| `type` | string | GeoJSON object type. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/contour/{serviceType}/{idType}/{idValue}.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-broadcast-contour.md) for the provider-specific parameters and requirements.

