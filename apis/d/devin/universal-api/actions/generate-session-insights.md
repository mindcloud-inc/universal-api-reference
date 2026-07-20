# Devin: Generate Session Insights

Generates session insights for a Devin session.

```
POST https://connect.mindcloud.co/v1/universal/devin/latest/actions/generate-session-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devin/latest/actions/generate-session-insights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "devinId": "string",
  "orgId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/generate-session-insights', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "devinId": "string",
    "orgId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `devinId` | string | yes | Session ID prefixed with devin-. |
| `orgId` | string | yes | Devin organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "session_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `session_id` | string | Devin session ID. |
| `status` | string | Insight generation status. |

## Native endpoint

Through the native Devin API, this operation is `POST /v3/organizations/:org_id/sessions/:devin_id/insights/generate` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-session-insights.md) for the provider-specific parameters and requirements.

