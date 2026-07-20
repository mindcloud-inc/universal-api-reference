# Status Hero: List reports



```
GET https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-reports?${params}`, {
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
      "completedStatusIds": [
        "string"
      ],
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metrics": {},
      "questionLabels": {},
      "questions": {},
      "teamId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedStatusIds` | array<string> |  |
| `date` | date |  |
| `id` | string |  |
| `metrics` | object |  |
| `questionLabels` | object |  |
| `questions` | object |  |
| `teamId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Status Hero API, this operation is `GET /reports` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

