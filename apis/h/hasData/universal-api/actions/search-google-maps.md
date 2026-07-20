# HasData: Search Google Maps

Retrieves Google Maps search results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-maps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-maps?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-maps?${params}`, {
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
| `ll` | string | no | Map coordinates in the format @lat,lng,zoomz. |
| `q` | string | yes | Search query for Google Maps. |
| `start` | number | no | Result offset for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "localResults": [
        {}
      ],
      "requestMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `localResults` | array<object> |  |
| `requestMetadata` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google-maps/search` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-maps.md) for the provider-specific parameters and requirements.

