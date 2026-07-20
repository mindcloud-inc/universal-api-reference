# Rowform: Test Authentication

Retrieves API key validation details from Rowform.

```
GET https://connect.mindcloud.co/v1/universal/rowform/latest/actions/test-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rowform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowform/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowform/latest/actions/test-authentication?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "key_name": "Ava Chen",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address associated with the authenticated Rowform API key. |
| `id` | string | Rowform identifier for the API key or principal. |
| `key_name` | string | Human-readable name assigned to the Rowform API key. |
| `name` | string | Display name associated with the authenticated Rowform API key. |
| `scopes` | array<string> | Scopes granted to the authenticated Rowform API key. |

## Native endpoint

Through the native Rowform API, this operation is `GET /api/zapier/auth` (base URL `https://app.rowform.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-authentication.md) for the provider-specific parameters and requirements.

