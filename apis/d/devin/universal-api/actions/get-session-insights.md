# Devin: Get Session Insights

Retrieves generated session insights from Devin.

```
GET https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-session-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-session-insights?connectionId=$CONNECTION_ID&devinId=string&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "devinId": "string",
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-session-insights?${params}`, {
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
| `devinId` | string | yes | Session ID prefixed with devin-. |
| `orgId` | string | yes | Devin organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "insights": {},
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
| `insights` | object | Generated insight data. |
| `session_id` | string | Devin session ID. |
| `status` | string | Insight generation status. |

## Native endpoint

Through the native Devin API, this operation is `GET /v3/organizations/:org_id/sessions/:devin_id/insights` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-insights.md) for the provider-specific parameters and requirements.

