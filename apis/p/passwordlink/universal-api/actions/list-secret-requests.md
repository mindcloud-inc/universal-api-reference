# Password.link: List Secret Requests



```
GET https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secret-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password.link `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secret-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secret-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "expiration": 1,
      "id": "string",
      "limit": 1,
      "message": "string",
      "secretDescription": "string",
      "secretExpiration": "string",
      "secretMaxViews": 1,
      "secretMessage": "string",
      "secretPassword": true,
      "sendToEmail": "ava@example.com",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The description for the secret request. |
| `expiration` | number | Expiration time in hours. |
| `id` | string | The secret request ID. |
| `limit` | number | Usage limit. |
| `message` | string | The message for the secret request. |
| `secretDescription` | string | The created secret description. |
| `secretExpiration` | string | The created secret expiration. |
| `secretMaxViews` | number | The created secret view limit. |
| `secretMessage` | string | The created secret message. |
| `secretPassword` | boolean | Whether the created secret is password-protected. |
| `sendToEmail` | string | Destination email address. |
| `templateId` | string | The template ID. |

## Native endpoint

Through the native Password.link API, this operation is `GET /secret_requests` (base URL `https://password.link/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-secret-requests.md) for the provider-specific parameters and requirements.

