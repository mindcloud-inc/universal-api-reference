# Zenclass: Create auto login link

Creates a one-click login link in Zenclass.

```
POST https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/create-auto-login-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenclass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/create-auto-login-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "redirectPath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/create-auto-login-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "redirectPath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Student email address. |
| `redirectPath` | string | yes | School-relative path to open after sign-in. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_login_link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_login_link` | string | One-time Zenclass auto-login URL. |

## Native endpoint

Through the native Zenclass API, this operation is `POST /api/v1/auto_login_link` (base URL `https://api.zenclass.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-auto-login-link.md) for the provider-specific parameters and requirements.

