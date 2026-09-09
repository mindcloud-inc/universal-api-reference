# Walmart: Bulk Item Setup - Retire Items

Permanently retire a list of Items identified by their SKU.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-retire-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-retire-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-setup-retire-items', {
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
| `items[]` | array<object> | no |  |
| `items[].sku` | string | no | The SKU to retire. |

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
| `feedId` | string | A unique identifier returned by the Bulk Upload API, use it to track and manage the status of a feed file. |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-item-setup-retire-items.md) for the provider-specific parameters and requirements.

