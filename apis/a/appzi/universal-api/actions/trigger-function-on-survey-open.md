# Appzi: Trigger Function On Survey Open

Generates an Appzi survey-open handler snippet.

```
POST https://connect.mindcloud.co/v1/universal/appzi/latest/actions/trigger-function-on-survey-open
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appzi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/trigger-function-on-survey-open" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appzi/latest/actions/trigger-function-on-survey-open', {
  method: 'POST',
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Appzi API returns.

## Native endpoint

Through the native Appzi API, this operation is `GET https://docs.appzi.io/integration/events/` (base URL `https://api.appzi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-function-on-survey-open.md) for the provider-specific parameters and requirements.

