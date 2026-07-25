# Kite Suite: Create Custom Field (Drag Endpoint)



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-custom-field-drag-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-custom-field-drag-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-custom-field-drag-endpoint', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/custom-field/drag` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field-drag-endpoint.md) for the provider-specific parameters and requirements.

