# Satiurn: Update Movement

Updates an existing financial movement in Satiurn.

```
PUT https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/update-movement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satiurn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/update-movement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/update-movement', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Satiurn API returns.

## Native endpoint

Through the native Satiurn API, this operation is `PUT /finance/movement` (base URL `https://publicapi.satiurn.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-movement.md) for the provider-specific parameters and requirements.

