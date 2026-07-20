# Aqara Home for US: Set Resource Info

Updates resource information for an Aqara device.

```
PUT https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/set-resource-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for US `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/set-resource-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/set-resource-info', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for US API returns.

## Native endpoint

Through the native Aqara Home for US API, this operation is `POST /` (base URL `https://open-usa.aqara.com/v3.0/open/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-resource-info.md) for the provider-specific parameters and requirements.

