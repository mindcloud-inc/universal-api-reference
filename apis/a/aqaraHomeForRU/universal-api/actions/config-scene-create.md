# Aqara Home for RU: Create Scene

Creates a scene in Aqara Home for RU.

```
POST https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-scene-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for RU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-scene-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-scene-create', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for RU API returns.

## Native endpoint

Through the native Aqara Home for RU API, this operation is `POST /v3.0/open/api` (base URL `https://open-ru.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/config-scene-create.md) for the provider-specific parameters and requirements.

