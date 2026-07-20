# PixieBrix: Get Current User

Retrieves the current user from PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-current-user?${params}`, {
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
      "deployment_key_account": true,
      "email": "ava@example.com",
      "enforce_update_millis": 1,
      "flags": [
        "string"
      ],
      "group_memberships": [
        {}
      ],
      "id": "string",
      "is_onboarded": true,
      "name": "Ava Chen",
      "organization": {},
      "organization_memberships": [
        {}
      ],
      "partner": "string",
      "scope": "string",
      "service_account": true,
      "test_account": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployment_key_account` | boolean |  |
| `email` | string |  |
| `enforce_update_millis` | number |  |
| `flags` | array<string> |  |
| `group_memberships` | array<object> |  |
| `id` | string |  |
| `is_onboarded` | boolean |  |
| `name` | string |  |
| `organization` | object |  |
| `organization_memberships` | array<object> |  |
| `partner` | string |  |
| `scope` | string |  |
| `service_account` | boolean |  |
| `test_account` | boolean |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/me/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

