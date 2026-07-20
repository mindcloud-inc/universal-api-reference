# LiveChat: List Routing Statuses

Retrieves agent routing statuses from LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-routing-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-routing-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-routing-statuses?${params}`, {
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
| `filters` | object | no | Routing status filters. Default: `{}`. |
| `filters.groupIds[]` | array<number> | no | Filter statuses by group IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Agent identifier. |
| `status` | string | Current routing status for the agent. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /list_routing_statuses` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-routing-statuses.md) for the provider-specific parameters and requirements.

