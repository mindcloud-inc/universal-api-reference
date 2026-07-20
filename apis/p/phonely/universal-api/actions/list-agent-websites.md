# Phonely: List Agent Websites

Retrieves agent websites from Phonely.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-agent-websites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-agent-websites?connectionId=$CONNECTION_ID&uid=string&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-agent-websites?${params}`, {
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
| `uid` | string | yes |  |
| `agentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "websites": [
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
| `websites` | array<object> | Website knowledge sources attached to the selected agent. |

## Native endpoint

Through the native Phonely API, this operation is `GET /api/agent-websites` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-websites.md) for the provider-specific parameters and requirements.

