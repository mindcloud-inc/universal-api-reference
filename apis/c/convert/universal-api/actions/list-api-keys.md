# Convert: List API Keys

Retrieves API keys from Convert for an account.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/list-api-keys?${params}`, {
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
      "auth_type": "string",
      "key_id": "string",
      "key_secret": "string",
      "name": "Ava Chen",
      "projects": [
        1
      ],
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth_type` | string | Authentication type for this API key. |
| `key_id` | string | Public identifier for the API key pair. |
| `key_secret` | string | Secret part of the API key pair; may be masked after creation. |
| `name` | string | Friendly name for the API key. |
| `projects` | array<number> | Project IDs this API key is authorized to access. |
| `role` | string | Role assigned to this API key. |

## Native endpoint

Through the native Convert API, this operation is `GET /accounts/:account_id/api-keys` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

