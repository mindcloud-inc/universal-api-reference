# Nyne AI: Check Company Feature

Retrieves feature detection details for a company from Nyne AI.

```
GET https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/check-company-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyne AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/check-company-feature?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/check-company-feature?${params}`, {
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
      "feature": {},
      "message": "string",
      "request_id": "string",
      "score": 1,
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
| `feature` | object | Feature assessment payload. |
| `message` | string | Provider status message. |
| `request_id` | string | Nyne request identifier. |
| `score` | number | Feature fit score when returned. |
| `status` | string | Processing status. |
| `success` | boolean | Whether the request completed or was accepted. |
| `timestamp` | date | Response timestamp. |

## Native endpoint

Through the native Nyne AI API, this operation is `POST /company/checkfeature` (base URL `https://api.nyne.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-company-feature.md) for the provider-specific parameters and requirements.

