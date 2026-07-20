# Verifalia: Delete Contact Method

Deletes an existing contact method from Verifalia.

```
DELETE https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/delete-contact-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/delete-contact-method?connectionId=$CONNECTION_ID&userId=string&contactMethodId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string",
  "contactMethodId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/delete-contact-method?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verifalia API returns.

## Native endpoint

Through the native Verifalia API, this operation is `DELETE /users/{user-id}/contact-methods/{contact-method-id}` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-method.md) for the provider-specific parameters and requirements.

