# Framework360: Test Webhook



```
PUT https://connect.mindcloud.co/v1/universal/framework360/latest/actions/webhooks-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/webhooks-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/webhooks-test', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `GET webhooks/test` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/webhooks-test.md) for the provider-specific parameters and requirements.

