# Onethread: Get Project Tracking



```
GET https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-project-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onethread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-project-tracking?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-project-tracking?${params}`, {
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
      "projectTracking": [
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
| `projectTracking` | array<object> |  |

## Native endpoint

Through the native Onethread API, this operation is `GET /track/project` (base URL `https://api.onethread.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-tracking.md) for the provider-specific parameters and requirements.

