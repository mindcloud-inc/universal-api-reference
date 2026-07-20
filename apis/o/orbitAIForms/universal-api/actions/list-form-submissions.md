# Orbit AI (Forms): List Form Submissions



```
GET https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-form-submissions?${params}`, {
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
      "fields": {},
      "id": "string",
      "metadata": {},
      "status": "string",
      "submitted_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `status` | string |  |
| `submitted_at` | date |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `GET /api/v1/forms/:id/submissions` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

