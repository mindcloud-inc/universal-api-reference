# Productboard: List All Releases

Retrieves releases from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-releases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-releases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-releases?${params}`, {
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
      "archived": true,
      "description": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "releaseGroup": {},
      "state": "string",
      "timeframe": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `links` | object |  |
| `name` | string |  |
| `releaseGroup` | object |  |
| `state` | string |  |
| `timeframe` | object |  |

## Native endpoint

Through the native Productboard API, this operation is `GET /releases` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-releases.md) for the provider-specific parameters and requirements.

