# Omnisend: List Custom Events

Retrieves custom events from Omnisend.

```
GET https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/list-custom-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/list-custom-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/list-custom-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `GET /v3/events` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-events.md) for the provider-specific parameters and requirements.

