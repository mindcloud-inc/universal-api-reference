# Hoops: Kill Session



```
DELETE https://connect.mindcloud.co/v1/universal/hoops/latest/actions/kill-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hoops/latest/actions/kill-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoops/latest/actions/kill-session?${params}`, {
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
| `sessionId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "killed": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `killed` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Hoops API, this operation is `POST /sessions/{session_id}/kill` (base URL `https://use.hoop.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kill-session.md) for the provider-specific parameters and requirements.

