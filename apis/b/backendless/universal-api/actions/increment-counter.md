# Backendless: Increment Counter

Increments a counter in Backendless.

```
PUT https://connect.mindcloud.co/v1/universal/backendless/latest/actions/increment-counter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Backendless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/backendless/latest/actions/increment-counter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/backendless/latest/actions/increment-counter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Backendless API returns.

## Native endpoint

Through the native Backendless API, this operation is `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/counters/{counterName}/increment/get` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/increment-counter.md) for the provider-specific parameters and requirements.

