# SMSINDIAHUB: Send International Flash SMS

Sends an international flash SMS in SMSINDIAHUB.

```
POST https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send-international-flash-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send-international-flash-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send-international-flash-sms', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSINDIAHUB API returns.

## Native endpoint

Through the native SMSINDIAHUB API, this operation is `GET http://international.smsindiahub.in/bulksms/bulksms` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-international-flash-sms.md) for the provider-specific parameters and requirements.

