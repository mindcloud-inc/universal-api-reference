# PrintNode: Simulate Test Scale Measurement

Simulates a test scale measurement in PrintNode.

```
PUT https://connect.mindcloud.co/v1/universal/printNode/latest/actions/simulate-test-scale-measurement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/simulate-test-scale-measurement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printNode/latest/actions/simulate-test-scale-measurement', {
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

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body because the PrintNode test-scale trigger endpoint returns HTTP 204 No Content. |

## Native endpoint

Through the native PrintNode API, this operation is `PUT /scale` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/simulate-test-scale-measurement.md) for the provider-specific parameters and requirements.

