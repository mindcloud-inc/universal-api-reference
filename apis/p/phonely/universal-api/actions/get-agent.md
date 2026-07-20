# Phonely: Get Agent

Retrieves an agent from Phonely.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-agent?connectionId=$CONNECTION_ID&uid=string&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-agent?${params}`, {
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
| `uid` | string | yes | The Phonely user ID that owns the target agent. |
| `agentId` | string | yes | The Phonely agent ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Agent ID. |
| `name` | string | Agent name. |
| `uid` | string | User ID associated with the agent. |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/get-agent` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

