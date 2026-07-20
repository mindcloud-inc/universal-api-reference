# Verifalia: Get Contact Method

Retrieves a contact method from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-contact-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-contact-method?connectionId=$CONNECTION_ID&userId=string&contactMethodId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string",
  "contactMethodId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-contact-method?${params}`, {
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
| `userId` | string | yes | The Verifalia user ID. |
| `contactMethodId` | string | yes | The Verifalia contact method ID. |

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

Through the native Verifalia API, this operation is `GET /users/{user-id}/contact-methods/{contact-method-id}` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-method.md) for the provider-specific parameters and requirements.

