# KEYZY: Update Activation

Updates a license activation in KEYZY.

```
PUT https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-activation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-activation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activated": true,
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-activation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activated": true,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activated` | boolean | yes | Set to true or false. |
| `id` | string | yes | ID of the activation object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Activation update confirmation message. |

## Native endpoint

Through the native KEYZY API, this operation is `PUT /activations/:id` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activation.md) for the provider-specific parameters and requirements.

