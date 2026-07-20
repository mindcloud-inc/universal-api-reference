# Verifalia: Create Contact Method

Creates a new contact method in Verifalia.

```
POST https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/create-contact-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/create-contact-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "type": "string",
  "displayName": "Ava Chen",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/create-contact-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "type": "string",
    "displayName": "Ava Chen",
    "emailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The Verifalia user ID. |
| `type` | string | yes | The contact method type. Verifalia currently supports only `Email`. |
| `displayName` | string | yes | A user-friendly label for the contact method. |
| `emailAddress` | string | yes | The email address to bind as a contact method. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedOn": "string",
      "createdOn": "string",
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "id": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedOn` | string | When the contact method was activated, if available. |
| `createdOn` | string | When the contact method was created. |
| `displayName` | string | The contact method display name. |
| `emailAddress` | string | The email address bound to the contact method. |
| `id` | string | The contact method ID. |
| `status` | string | The contact method status. |
| `type` | string | The contact method type. |

## Native endpoint

Through the native Verifalia API, this operation is `POST /users/{user-id}/contact-methods` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-method.md) for the provider-specific parameters and requirements.

