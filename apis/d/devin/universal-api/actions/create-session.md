# Devin: Create Session

Creates a new session in Devin.

```
POST https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orgId": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orgId": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgId` | string | yes | Devin organization ID. |
| `prompt` | string | yes | Prompt for the new Devin session. |
| `title` | string | no | Optional title for the session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "org_id": "string",
      "session_id": "string",
      "status": "string",
      "status_detail": "string",
      "title": "string",
      "updated_at": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number | Creation timestamp. |
| `org_id` | string | Organization ID. |
| `session_id` | string | Created Devin session ID. |
| `status` | string | Session status. |
| `status_detail` | string | Detailed session status. |
| `title` | string | Session title. |
| `updated_at` | number | Update timestamp. |
| `url` | string | Devin session URL. |

## Native endpoint

Through the native Devin API, this operation is `POST /v3/organizations/:org_id/sessions` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

