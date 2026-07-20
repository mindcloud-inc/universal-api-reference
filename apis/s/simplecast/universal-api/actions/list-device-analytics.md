# Simplecast: List Device Analytics

Retrieves device analytics from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-device-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-device-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-device-analytics?${params}`, {
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
      "collection": [
        {}
      ],
      "href": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> |  |
| `href` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Simplecast API, this operation is `GET /analytics/technology/devices` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-analytics.md) for the provider-specific parameters and requirements.

