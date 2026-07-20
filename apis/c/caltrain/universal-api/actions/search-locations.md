# Caltrain: Search Locations

Finds Caltrain locations by search query.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/search-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/search-locations?connectionId=$CONNECTION_ID&query=Millbrae" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Millbrae"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/search-locations?${params}`, {
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
| `query` | string | yes | Location text to search for. Example: `Millbrae`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "latitude": "string",
      "longitude": "string",
      "nid": "string",
      "text": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `latitude` | string |  |
| `longitude` | string |  |
| `nid` | string |  |
| `text` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /search/location_autocomplete` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-locations.md) for the provider-specific parameters and requirements.

