# Aqara Home for US: Create Position

Creates a new position in Aqara Home for US.

```
POST https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/create-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for US `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/create-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/create-position', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for US API returns.

## Native endpoint

Through the native Aqara Home for US API, this operation is `POST /` (base URL `https://open-usa.aqara.com/v3.0/open/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-position.md) for the provider-specific parameters and requirements.

