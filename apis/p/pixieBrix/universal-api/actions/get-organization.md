# PixieBrix: Get Organization

Retrieves an organization from PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationPk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationPk": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-organization?${params}`, {
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
| `organizationPk` | string | yes | PixieBrix organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_default_chat_copilot": true,
      "default_role": 1,
      "enable_invitations": true,
      "enforce_update_millis": 1,
      "id": "string",
      "members": [
        {}
      ],
      "name": "Ava Chen",
      "scope": "string",
      "session_idle_timeout_minutes": 1,
      "trial_end_timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_default_chat_copilot` | boolean |  |
| `default_role` | number |  |
| `enable_invitations` | boolean |  |
| `enforce_update_millis` | number |  |
| `id` | string |  |
| `members` | array<object> |  |
| `name` | string |  |
| `scope` | string |  |
| `session_idle_timeout_minutes` | number |  |
| `trial_end_timestamp` | date |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/organizations/:organization_pk/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

