# Samsara: List Addresses



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-addresses?${params}`, {
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
      "addressTypes": [
        "string"
      ],
      "createdAtTime": "string",
      "formattedAddress": "string",
      "geofence": {
        "polygon": {
          "vertices": [
            {
              "latitude": 1,
              "longitude": 1
            }
          ]
        },
        "settings": {
          "showAddresses": true
        }
      },
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "notes": "string",
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
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
| `addressTypes` | array<string> |  |
| `createdAtTime` | string |  |
| `formattedAddress` | string |  |
| `geofence.polygon.vertices[].latitude` | number |  |
| `geofence.polygon.vertices[].longitude` | number |  |
| `geofence.settings.showAddresses` | boolean |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET addresses` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

