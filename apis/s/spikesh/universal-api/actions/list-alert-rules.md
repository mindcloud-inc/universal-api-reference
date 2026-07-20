# Spike.sh: List Alert Rules

Retrieves alert rules for a team in Spike.sh.

```
GET https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/list-alert-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spike.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/list-alert-rules?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/list-alert-rules?${params}`, {
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
| `teamId` | string | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Spike.sh API returns.

## Native endpoint

Through the native Spike.sh API, this operation is `GET /automation/rules` (base URL `https://api.spike.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-rules.md) for the provider-specific parameters and requirements.

