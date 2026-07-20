# Better Stack Uptime: Get Incident

Retrieves an incident from Better Stack Uptime.

```
GET https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-incident?connectionId=$CONNECTION_ID&incidentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "incidentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-incident?${params}`, {
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
| `incidentId` | string | yes | Incident ID from Better Stack Uptime. |
| `teamName` | string | no | Better Stack team name when required by the token scope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `GET /v3/incidents/:incidentId` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-incident.md) for the provider-specific parameters and requirements.

