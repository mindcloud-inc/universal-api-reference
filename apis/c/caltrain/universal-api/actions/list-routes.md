# Caltrain: List Routes

Retrieves Caltrain routes.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-routes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-routes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "fieldRouteShortName": [
        {
          "value": "Ava Chen"
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
      "geojson": {
        "coordinates": [
          "string"
        ],
        "properties": {
          "agency": "string",
          "id": "string",
          "label": "string",
          "routeId": "string",
          "url": "https://example.com"
        },
        "type": "string"
      },
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
| `fieldRouteColor[].value` | string |  |
| `fieldRouteId[].value` | string |  |
| `fieldRouteShortName[].value` | string |  |
| `fieldTextColor[].value` | string |  |
| `fieldWeight[].value` | string |  |
| `geojson.coordinates[]` | string |  |
| `geojson.properties.agency` | string |  |
| `geojson.properties.id` | string |  |
| `geojson.properties.label` | string |  |
| `geojson.properties.routeId` | string |  |
| `geojson.properties.url` | string |  |
| `geojson.type` | string |  |
| `nid[].value` | string |  |
| `path[].alias` | string |  |
| `path[].langcode` | string |  |
| `path[].pid` | string |  |
| `title[].value` | string |  |
| `type[].targetId` | string |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/routes/all` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-routes.md) for the provider-specific parameters and requirements.

