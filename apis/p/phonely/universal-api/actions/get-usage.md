# Phonely: Get Usage

Retrieves usage from Phonely.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-usage?connectionId=$CONNECTION_ID&uid=string&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-usage?${params}`, {
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
| `uid` | string | yes | The Phonely user ID whose usage should be summarized. |
| `startDate` | string | yes | The inclusive start date for the usage window. |
| `endDate` | string | yes | The inclusive end date for the usage window. |
| `agentId` | string | no | Optionally restrict usage results to a single agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agents": [
        {}
      ],
      "dateRange": {},
      "requestedAgentId": "string",
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | array<object> | Per-agent usage rows for the requested date range. |
| `dateRange` | object | Resolved usage date range. |
| `requestedAgentId` | string | Agent ID filter echoed when usage is restricted to one agent. |
| `summary` | object | Top-level usage totals for the requested date range. |

## Native endpoint

Through the native Phonely API, this operation is `GET /api/usage` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

