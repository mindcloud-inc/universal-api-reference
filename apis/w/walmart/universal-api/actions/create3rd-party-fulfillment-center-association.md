# Walmart: Create 3rd Party Fulfillment Center Association

Associate a third party fulfillment center with Seller.

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/create3rd-party-fulfillment-center-association
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/create3rd-party-fulfillment-center-association" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/create3rd-party-fulfillment-center-association', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipNode[].shipNode` | string | no | The fulfillment center (ship node) which uniquely identifies each facility and is retrieved from the `List 3PL Providers` action. |
| `shipNodeHeader` | object | no |  |
| `shipNodeHeader.version` | string | no | Example: `1.2` |
| `shipNode[]` | array | no |  |
| `shipNode[].status` | list | no | Status of fulfillment center. Allowed values: `ACTIVE`, `INACTIVE` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shipNode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipNode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/settings/shipping/3plshipnodes` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create3rd-party-fulfillment-center-association.md) for the provider-specific parameters and requirements.

