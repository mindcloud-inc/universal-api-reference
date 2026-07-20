# Caltrain: Get Stop Alerts

Retrieves alerts for a Caltrain stop.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-alerts?connectionId=$CONNECTION_ID&stopId=22nd_street" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stopId": "22nd_street"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-alerts?${params}`, {
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
| `stopId` | string | yes | Caltrain stop identifier such as 22nd_street. Example: `22nd_street`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "stop": {
          "childStopIds": {
            "7075": "string",
            "7076": "string",
            "11226": "string",
            "11227": "string"
          },
          "fieldAgencyId": [
            {
              "value": "string"
            }
          ],
          "fieldAmenitiesBenefits": [
            {
              "targetId": "string",
              "targetRevisionId": "string"
            }
          ],
          "fieldBody": [
            {
              "targetId": "string",
              "targetRevisionId": "string"
            }
          ],
          "fieldImage": [
            {
              "targetId": "string"
            }
          ],
          "fieldLocation": [
            {
              "bottom": 1,
              "geohash": "string",
              "geoType": "string",
              "lat": 1,
              "latlon": "string",
              "left": 1,
              "lon": 1,
              "right": 1,
              "top": 1,
              "value": "string"
            }
          ],
          "fieldLocationType": [
            {
              "value": "string"
            }
          ],
          "fieldServicedRoutes": [
            {
              "targetId": "string"
            }
          ],
          "fieldStopId": [
            {
              "value": "string"
            }
          ],
          "fieldTransitConnections": [
            {
              "targetId": "string",
              "targetRevisionId": "string"
            }
          ],
          "nid": [
            {
              "value": "string"
            }
          ],
          "path": [
            {
              "alias": "string",
              "langcode": "string",
              "pid": "string"
            }
          ],
          "title": [
            {
              "value": "string"
            }
          ],
          "type": [
            {
              "targetId": "string"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.stop.childStopIds.11226` | string |  |
| `meta.stop.childStopIds.11227` | string |  |
| `meta.stop.childStopIds.7075` | string |  |
| `meta.stop.childStopIds.7076` | string |  |
| `meta.stop.fieldAgencyId[].value` | string |  |
| `meta.stop.fieldAmenitiesBenefits[].targetId` | string |  |
| `meta.stop.fieldAmenitiesBenefits[].targetRevisionId` | string |  |
| `meta.stop.fieldBody[].targetId` | string |  |
| `meta.stop.fieldBody[].targetRevisionId` | string |  |
| `meta.stop.fieldImage[].targetId` | string |  |
| `meta.stop.fieldLocation[].bottom` | number |  |
| `meta.stop.fieldLocation[].geohash` | string |  |
| `meta.stop.fieldLocation[].geoType` | string |  |
| `meta.stop.fieldLocation[].lat` | number |  |
| `meta.stop.fieldLocation[].latlon` | string |  |
| `meta.stop.fieldLocation[].left` | number |  |
| `meta.stop.fieldLocation[].lon` | number |  |
| `meta.stop.fieldLocation[].right` | number |  |
| `meta.stop.fieldLocation[].top` | number |  |
| `meta.stop.fieldLocation[].value` | string |  |
| `meta.stop.fieldLocationType[].value` | string |  |
| `meta.stop.fieldServicedRoutes[].targetId` | string |  |
| `meta.stop.fieldStopId[].value` | string |  |
| `meta.stop.fieldTransitConnections[].targetId` | string |  |
| `meta.stop.fieldTransitConnections[].targetRevisionId` | string |  |
| `meta.stop.nid[].value` | string |  |
| `meta.stop.path[].alias` | string |  |
| `meta.stop.path[].langcode` | string |  |
| `meta.stop.path[].pid` | string |  |
| `meta.stop.title[].value` | string |  |
| `meta.stop.type[].targetId` | string |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/stops/:stopId/alerts` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stop-alerts.md) for the provider-specific parameters and requirements.

