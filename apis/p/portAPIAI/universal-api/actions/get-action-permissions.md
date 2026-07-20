# Port API AI: Get Action Permissions

Retrieves action permissions from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-action-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-action-permissions?connectionId=$CONNECTION_ID&actionIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-action-permissions?${params}`, {
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
| `actionIdentifier` | string | yes | The action identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "permissions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `permissions` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /actions/:action_identifier/permissions` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-permissions.md) for the provider-specific parameters and requirements.

