# Optform: List Lead Scores

Retrieves lead scores from Optform.

```
GET https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-lead-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-lead-scores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-lead-scores?${params}`, {
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
      "accountId": "string",
      "contactId": "string",
      "formId": "string",
      "id": 1,
      "questions": 1,
      "score": 1,
      "totalScore": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `contactId` | string |  |
| `formId` | string |  |
| `id` | number |  |
| `questions` | number |  |
| `score` | number |  |
| `totalScore` | number |  |

## Native endpoint

Through the native Optform API, this operation is `GET /data/api/score` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-scores.md) for the provider-specific parameters and requirements.

