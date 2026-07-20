# Status Hero: Get report



```
GET https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-report?connectionId=$CONNECTION_ID&id=2026-04-24" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2026-04-24"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-report?${params}`, {
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
| `id` | string | yes | The report ID or report date in YYYY-MM-DD format. Example: `2026-04-24`. |

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

Through the native Status Hero API, this operation is `GET /reports/:id` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

