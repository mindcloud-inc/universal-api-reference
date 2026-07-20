# Aqara Home for RU: Enable Linkage

Enables or disables a linkage in Aqara Home for RU.

```
PUT https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-linkage-enable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for RU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-linkage-enable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-linkage-enable', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for RU API returns.

## Native endpoint

Through the native Aqara Home for RU API, this operation is `POST /v3.0/open/api` (base URL `https://open-ru.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/config-linkage-enable.md) for the provider-specific parameters and requirements.

