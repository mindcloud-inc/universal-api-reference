# Quantcast: List Creatives

Retrieves creatives from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-creatives
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-creatives?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-creatives?${params}`, {
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
      "creatives": {
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
| `creatives` | object | Creatives connection returned by Quantcast. |
| `creatives.edges` | array<object> | Creative nodes in the result set. |
| `creatives.edges.id` | number | Quantcast creative identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-creatives.md) for the provider-specific parameters and requirements.

