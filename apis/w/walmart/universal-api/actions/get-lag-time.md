# Walmart: Get Lag Time

Rretrieve Lag Time for an item with a given SKU.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-lag-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-lag-time?connectionId=$CONNECTION_ID&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-lag-time?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sku` | string | yes | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. This will be used by the seller in the XSD file to refer to each item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fulfillmentLagTime": 1,
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fulfillmentLagTime` | number |  |
| `sku` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/lagtime` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lag-time.md) for the provider-specific parameters and requirements.

