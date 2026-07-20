# Timeular: V3 Unsubscribe all for User

Deletes current-user webhook subscriptions from the Timeular v3 API.

```
DELETE https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-unsubscribe-all-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-unsubscribe-all-for-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-unsubscribe-all-for-user?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `DELETE /api/v3/webhooks/subscription` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-unsubscribe-all-for-user.md) for the provider-specific parameters and requirements.

