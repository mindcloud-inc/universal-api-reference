# Feathery: Create Hidden Field



```
POST https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-hidden-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-hidden-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "field_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-hidden-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "field_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `field_id` | string | yes | A new unique ID for the hidden field to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_id` | string | The created hidden field ID. |

## Native endpoint

Through the native Feathery API, this operation is `POST /api/form/hidden_field/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hidden-field.md) for the provider-specific parameters and requirements.

