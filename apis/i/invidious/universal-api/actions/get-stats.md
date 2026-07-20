# Invidious: Get Stats



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-stats?${params}`, {
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
      "metadata": {
        "updatedAt": 1
      },
      "openRegistrations": true,
      "software": {
        "name": "Ava Chen",
        "version": "string"
      },
      "usage": {
        "users": {
          "activeHalfyear": 1,
          "total": 1
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
| `metadata.updatedAt` | number |  |
| `openRegistrations` | boolean |  |
| `software.name` | string |  |
| `software.version` | string |  |
| `usage.users.activeHalfyear` | number |  |
| `usage.users.total` | number |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /stats` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stats.md) for the provider-specific parameters and requirements.

