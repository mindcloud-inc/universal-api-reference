# Quantcast: List Metro Areas

Retrieves metro areas from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-metro-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-metro-areas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-metro-areas?${params}`, {
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
      "metroAreas": {
        "edges": {
          "id": 1
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
| `metroAreas` | object | Metro areas connection returned by Quantcast. |
| `metroAreas.edges` | array<object> | Metro area nodes in the result set. |
| `metroAreas.edges.id` | number | Quantcast metro area identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-metro-areas.md) for the provider-specific parameters and requirements.

