# Caltrain: List Nearby Stops

Finds Caltrain stops near a location.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-nearby-stops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-nearby-stops?connectionId=$CONNECTION_ID&longitude=-122.392492&latitude=37.756972&radius=0.1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "longitude": "-122.392492",
  "latitude": "37.756972",
  "radius": "0.1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-nearby-stops?${params}`, {
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
| `longitude` | number | yes | Longitude near the target stop search area. Example: `-122.392492`. |
| `latitude` | number | yes | Latitude near the target stop search area. Example: `37.756972`. |
| `radius` | number | yes | Search radius in miles. Example: `0.1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldAgencyId": [
        {
          "value": "string"
        }
      ],
      "fieldDirections": [
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
          "fieldAgencyId": [
            {
              "value": "string"
            }
          ],
          "fieldRouteId": [
            {
              "value": "string"
            }
          ],
          "fieldRouteShortName": [
            {
              "value": "Ava Chen"
            }
          ],
          "fieldSchedule": [
            {
              "targetId": "string"
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
      ],
      "fieldStopId": [
        {
          "value": "string"
        }
      ],
      "fieldZoneId": [
        {
          "value": "string"
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldAgencyId[].value` | string |  |
| `fieldDirections[].targetId` | string |  |
| `fieldDirections[].targetRevisionId` | string |  |
| `fieldImage[].targetId` | string |  |
| `fieldLocation[].bottom` | number |  |
| `fieldLocation[].geohash` | string |  |
| `fieldLocation[].geoType` | string |  |
| `fieldLocation[].lat` | number |  |
| `fieldLocation[].latlon` | string |  |
| `fieldLocation[].left` | number |  |
| `fieldLocation[].lon` | number |  |
| `fieldLocation[].right` | number |  |
| `fieldLocation[].top` | number |  |
| `fieldLocation[].value` | string |  |
| `fieldLocationType[].value` | string |  |
| `fieldServicedRoutes[].fieldAgencyId[].value` | string |  |
| `fieldServicedRoutes[].fieldRouteId[].value` | string |  |
| `fieldServicedRoutes[].fieldRouteShortName[].value` | string |  |
| `fieldServicedRoutes[].fieldSchedule[].targetId` | string |  |
| `fieldServicedRoutes[].fieldTransitConnections[].targetId` | string |  |
| `fieldServicedRoutes[].fieldTransitConnections[].targetRevisionId` | string |  |
| `fieldServicedRoutes[].nid[].value` | string |  |
| `fieldServicedRoutes[].path[].alias` | string |  |
| `fieldServicedRoutes[].path[].langcode` | string |  |
| `fieldServicedRoutes[].path[].pid` | string |  |
| `fieldServicedRoutes[].title[].value` | string |  |
| `fieldServicedRoutes[].type[].targetId` | string |  |
| `fieldStopId[].value` | string |  |
| `fieldZoneId[].value` | string |  |
| `nid[].value` | string |  |
| `path[].alias` | string |  |
| `path[].langcode` | string |  |
| `path[].pid` | string |  |
| `title[].value` | string |  |
| `type[].targetId` | string |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/stops/nearby/:longitude/:latitude/:radius` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nearby-stops.md) for the provider-specific parameters and requirements.

