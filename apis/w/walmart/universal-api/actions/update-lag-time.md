# Walmart: Update Lag Time

Update of lag time for items in bulk.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-lag-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-lag-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-lag-time', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lagTime[].additionalAttributes[].name` | string | no |  |
| `lagTime[].sku` | string | no | A seller-provided Product ID. |
| `lagTimeHeader.version` | string | no | Default: `1.0`. Example: `1.0`. |
| `lagTime[].additionalAttributes[].value` | string | no |  |
| `lagTime[].fulfillmentLagTime` | number | no | The # of days between when the item is ordered and when it is shipped. |
| `lagTimeHeader.feedDate` | string | no |  |
| `lagTime[].additionalAttributes[]` | array | no |  |
| `lagTime[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feedId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lag-time.md) for the provider-specific parameters and requirements.

