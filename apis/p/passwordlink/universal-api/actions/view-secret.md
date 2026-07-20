# Password.link: View Secret



```
GET https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/view-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password.link `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/view-secret?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/view-secret?${params}`, {
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
| `id` | string | yes | Password.link secret identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ciphertext": "string",
      "id": "string",
      "message": "string",
      "passwordPartPrivate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ciphertext` | string | The ciphertext of the secret. |
| `id` | string | The secret ID. |
| `message` | string | The message for the secret, if set. |
| `passwordPartPrivate` | string | The private password part of the secret. |

## Native endpoint

Through the native Password.link API, this operation is `GET /secrets/:id` (base URL `https://password.link/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-secret.md) for the provider-specific parameters and requirements.

