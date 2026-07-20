# SVAHNAR: Login



```
GET https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/login?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeIds` | boolean | no | Whether to include user IDs in the login response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "request_metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address of the authenticated user. |
| `first_name` | string | First name of the authenticated user. |
| `last_name` | string | Last name of the authenticated user. |
| `request_metadata` | object | Optional response metadata including the request ID. |

## Native endpoint

Through the native SVAHNAR API, this operation is `POST /v1/auth/login` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login.md) for the provider-specific parameters and requirements.

