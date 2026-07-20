# Quo: Get Call Summary

Retrieves a summary for a Quo call.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-summary?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-summary?${params}`, {
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
| `callId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "jobs": [
        {}
      ],
      "nextSteps": [
        "string"
      ],
      "status": "string",
      "summary": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string |  |
| `jobs` | array<object> |  |
| `nextSteps` | array<string> |  |
| `status` | string |  |
| `summary` | array<string> |  |

## Native endpoint

Through the native Quo API, this operation is `GET /call-summaries/:callId` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-summary.md) for the provider-specific parameters and requirements.

