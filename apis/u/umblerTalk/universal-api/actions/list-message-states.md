# Umbler Talk: List Message States

Retrieves a message's state history from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-message-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-message-states?connectionId=$CONNECTION_ID&id=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-message-states?${params}`, {
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
| `id` | string | yes | The message ID. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "states": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `states` | array<object> |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/messages/[:id]/states/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-states.md) for the provider-specific parameters and requirements.

