# Password.link: Create Secret



```
POST https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password.link `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ciphertext": "string",
  "passwordPartPrivate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ciphertext": "string",
    "passwordPartPrivate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ciphertext` | string | yes | SJCL-compatible Base64 ciphertext for the secret. |
| `passwordPartPrivate` | string | yes | Private password part in Base64. |
| `description` | string | no | Optional secret description. |
| `message` | string | no | Optional message shown with the secret. |
| `expiration` | number | no | Expiration time in hours. |
| `viewButton` | boolean | no | Show a view secret button instead of showing the secret immediately. |
| `captcha` | boolean | no | Show a simple CAPTCHA before showing the secret. |
| `password` | string | no | Optional password required to view the secret. |
| `maxViews` | number | no | Maximum number of times the secret can be viewed. Possible values are 1-100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The created secret ID. |

## Native endpoint

Through the native Password.link API, this operation is `POST /secrets` (base URL `https://password.link/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-secret.md) for the provider-specific parameters and requirements.

