# Port API AI: Get Action Automation

Retrieves an action automation from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-action-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-action-automation?connectionId=$CONNECTION_ID&actionIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-action-automation?${params}`, {
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
      "action": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /actions/:action_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-automation.md) for the provider-specific parameters and requirements.

