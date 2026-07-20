# Leadboxer: Retrieve Lead Events

Retrieves lead events in Leadboxer by session ID.

```
GET https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-lead-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-lead-events?connectionId=$CONNECTION_ID&sessionId=string&limit=1&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "limit": "1",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-lead-events?${params}`, {
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
| `sessionId` | string | yes |  |
| `limit` | number | yes |  |
| `site` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `GET /v1/leads/events` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-lead-events.md) for the provider-specific parameters and requirements.

