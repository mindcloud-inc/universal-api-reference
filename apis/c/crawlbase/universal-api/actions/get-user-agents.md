# Crawlbase: Get User Agents

Retrieves random user-agent strings from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-user-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-user-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-user-agents?${params}`, {
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
| `device` | list | no | Optional device category for random user agents: desktop or mobile. One of: `0`, `1`. |
| `size` | number | no | Optional number of user agents to return. Crawlbase documents a maximum of 10 and default of 1. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agents": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | array<string> | Random user agents returned by Crawlbase. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /user_agents` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-agents.md) for the provider-specific parameters and requirements.

