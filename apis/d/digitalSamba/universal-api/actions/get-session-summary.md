# Digital Samba: Get session summary

Retrieves a session summary from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-summary?connectionId=$CONNECTION_ID&session=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-summary?${params}`, {
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
| `session` | string | yes | Session path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Summary generation job identifier. |
| `status` | string | Summary status, such as IN_PROGRESS or READY. |
| `summary` | string | Generated session summary text. |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /sessions/:session/summary` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-summary.md) for the provider-specific parameters and requirements.

