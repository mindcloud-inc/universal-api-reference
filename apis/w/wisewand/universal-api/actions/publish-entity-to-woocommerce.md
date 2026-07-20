# Wisewand: Publish entity to WooCommerce

Publishes a Wisewand entity to WooCommerce.

```
POST https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/publish-entity-to-woocommerce
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/publish-entity-to-woocommerce" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity_id": "test-id",
  "connection_id": "test-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/publish-entity-to-woocommerce', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity_id": "test-id",
    "connection_id": "test-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity_id` | string | yes | The ID of the entity to publish Default: `test-id`. |
| `connection_id` | string | yes | The ID of the WooCommerce connection to use Default: `test-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Operation result. |

## Native endpoint

Through the native Wisewand API, this operation is `POST /v1/publish/woocommerce/:entity_id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-entity-to-woocommerce.md) for the provider-specific parameters and requirements.

