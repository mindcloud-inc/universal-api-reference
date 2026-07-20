# Password.link: List Secrets



```
GET https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secrets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password.link `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secrets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secrets?${params}`, {
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
      "captcha": true,
      "createdAt": "string",
      "description": "string",
      "expiration": 1,
      "expired": true,
      "id": "string",
      "maxViews": 1,
      "message": "string",
      "password": true,
      "viewButton": true,
      "views": [
        {}
      ],
      "viewTimes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `captcha` | boolean | Whether CAPTCHA is enabled. |
| `createdAt` | string | When the secret was created. |
| `description` | string | The description for the secret. |
| `expiration` | number | Expiration time in hours. |
| `expired` | boolean | Whether the secret has expired. |
| `id` | string | The secret ID. |
| `maxViews` | number | The maximum number of views. |
| `message` | string | The message for the secret. |
| `password` | boolean | Whether the secret has a password. |
| `viewButton` | boolean | Whether the view secret button is enabled. |
| `views` | array<object> | Secret view records. |
| `viewTimes` | number | How many times the secret has been viewed. |

## Native endpoint

Through the native Password.link API, this operation is `GET /secrets` (base URL `https://password.link/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-secrets.md) for the provider-specific parameters and requirements.

