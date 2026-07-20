# Verifalia: Update Contact Method

Updates an existing contact method in Verifalia.

```
PUT https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/update-contact-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/update-contact-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "contactMethodId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/update-contact-method', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "contactMethodId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The Verifalia user ID. |
| `contactMethodId` | string | yes | The Verifalia contact method ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verifalia API returns.

## Native endpoint

Through the native Verifalia API, this operation is `PATCH /users/{user-id}/contact-methods/{contact-method-id}` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-method.md) for the provider-specific parameters and requirements.

