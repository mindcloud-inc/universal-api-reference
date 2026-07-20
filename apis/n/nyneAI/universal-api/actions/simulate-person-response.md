# Nyne AI: Simulate Person Response

Retrieves a simulated response from a person in Nyne AI.

```
GET https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/simulate-person-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyne AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/simulate-person-response?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/simulate-person-response?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_on": "2026-05-07T12:00:00.000Z",
      "message": "string",
      "request_id": "string",
      "response": "string",
      "simulation": {},
      "status": "string",
      "success": true,
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_on` | date | Job creation timestamp. |
| `message` | string | Provider status message. |
| `request_id` | string | Nyne request identifier. |
| `response` | string | Simulated response text when available. |
| `simulation` | object | Simulation payload when available. |
| `status` | string | Processing status. |
| `success` | boolean | Whether the request was accepted. |
| `timestamp` | date | Response timestamp. |

## Native endpoint

Through the native Nyne AI API, this operation is `POST /person/simulation` (base URL `https://api.nyne.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/simulate-person-response.md) for the provider-specific parameters and requirements.

