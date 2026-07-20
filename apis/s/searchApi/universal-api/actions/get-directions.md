# SearchApi: Get Directions



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-directions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-directions?connectionId=$CONNECTION_ID&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-directions?${params}`, {
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
| `from` | string | yes | Departure location. |
| `to` | string | yes | Arrival location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directions": [
        {}
      ],
      "placesInfo": [
        {}
      ],
      "searchMetadata": {},
      "searchParameters": {},
      "travelModes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directions` | array<object> |  |
| `placesInfo` | array<object> |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |
| `travelModes` | array<object> |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-directions.md) for the provider-specific parameters and requirements.

