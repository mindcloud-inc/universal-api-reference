# Jooto: List Public Notifications

Retrieves a list of public notifications from Jooto.

```
GET https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jooto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-notifications?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jooto API returns.

## Native endpoint

Through the native Jooto API, this operation is `GET /api/public/v1/notifications` (base URL `https://app.jooto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-notifications.md) for the provider-specific parameters and requirements.

