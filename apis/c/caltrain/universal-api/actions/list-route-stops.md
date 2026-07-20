# Caltrain: List Route Stops

Retrieves stops for a Caltrain route.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-route-stops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-route-stops?connectionId=$CONNECTION_ID&routeId=Limited" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "routeId": "Limited"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-route-stops?${params}`, {
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
| `routeId` | string | yes | Caltrain route identifier such as Limited or Express. Example: `Limited`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childStopIds": {
        "7113": "string",
        "7114": "string",
        "11230": "string"
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
      "fieldHistory": [
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
          "fieldRouteColor": [
            {
              "value": "string"
            }
          ],
          "fieldRouteId": [
            {
              "value": "string"
            }
          ],
          "fieldTextColor": [
            {
              "value": "string"
            }
          ],
          "fieldWeight": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childStopIds.11230` | string |  |
| `childStopIds.7113` | string |  |
| `childStopIds.7114` | string |  |
| `fieldAgencyId[].value` | string |  |
| `fieldAmenitiesBenefits[].targetId` | string |  |
| `fieldAmenitiesBenefits[].targetRevisionId` | string |  |
| `fieldBody[].targetId` | string |  |
| `fieldBody[].targetRevisionId` | string |  |
| `fieldHistory[].targetId` | string |  |
| `fieldHistory[].targetRevisionId` | string |  |
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
| `fieldServicedRoutes[].fieldRouteColor[].value` | string |  |
| `fieldServicedRoutes[].fieldRouteId[].value` | string |  |
| `fieldServicedRoutes[].fieldTextColor[].value` | string |  |
| `fieldServicedRoutes[].fieldWeight[].value` | string |  |
| `fieldServicedRoutes[].nid[].value` | string |  |
| `fieldServicedRoutes[].path[].alias` | string |  |
| `fieldServicedRoutes[].path[].langcode` | string |  |
| `fieldServicedRoutes[].path[].pid` | string |  |
| `fieldServicedRoutes[].title[].value` | string |  |
| `fieldServicedRoutes[].type[].targetId` | string |  |
| `fieldStopId[].value` | string |  |
| `fieldTransitConnections[].targetId` | string |  |
| `fieldTransitConnections[].targetRevisionId` | string |  |
| `nid[].value` | string |  |
| `path[].alias` | string |  |
| `path[].langcode` | string |  |
| `path[].pid` | string |  |
| `title[].value` | string |  |
| `type[].targetId` | string |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/routes/:routeId/stops` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-route-stops.md) for the provider-specific parameters and requirements.

