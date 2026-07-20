# Vero: Resubscribe

Resubscribes a user in Vero globally.

```
PUT https://connect.mindcloud.co/v1/universal/vero/latest/actions/resubscribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vero/latest/actions/resubscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/resubscribe', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the user to resubscribe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable Vero result message. |
| `status` | number | HTTP-style status code returned by Vero. |

## Native endpoint

Through the native Vero API, this operation is `POST /api/v2/users/resubscribe` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resubscribe.md) for the provider-specific parameters and requirements.

