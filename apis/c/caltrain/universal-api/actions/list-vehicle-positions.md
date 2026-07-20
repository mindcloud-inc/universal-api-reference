# Caltrain: Get Vehicle Positions Feed

Retrieves the Caltrain vehicle positions feed.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-vehicle-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-vehicle-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-vehicle-positions?${params}`, {
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
      "Entities": [
        {}
      ],
      "Header": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Entities` | array<object> |  |
| `Header` | object |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /files/rt/vehiclepositions/CT.json` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicle-positions.md) for the provider-specific parameters and requirements.

