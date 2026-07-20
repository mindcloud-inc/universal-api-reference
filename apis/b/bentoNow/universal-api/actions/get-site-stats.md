# Bento Now: Get Site Stats

Retrieves site subscriber statistics from Bento Now.

```
GET https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-site-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-site-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-site-stats?${params}`, {
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
      "subscriberCount": 1,
      "unsubscriberCount": 1,
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriberCount` | number |  |
| `unsubscriberCount` | number |  |
| `userCount` | number |  |

## Native endpoint

Through the native Bento Now API, this operation is `GET /v1/stats/site` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-stats.md) for the provider-specific parameters and requirements.

