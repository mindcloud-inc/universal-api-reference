# Phonely: List Agents

Retrieves agents from Phonely.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-agents?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-agents?${params}`, {
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
| `uid` | string | yes | Your user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "businessPhoneNumber": "string",
      "country": "string",
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
| `businessPhoneNumber` | string | Business phone number, when available. |
| `country` | string | Agent country, when available. |
| `name` | string | Agent name. |
| `uid` | string | User ID associated with the agent. |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/get-agents` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

