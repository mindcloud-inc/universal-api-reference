# CheckFlow: Get Analytics



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-analytics?connectionId=$CONNECTION_ID&periodStartDate=2026-03-20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "periodStartDate": "2026-03-20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-analytics?${params}`, {
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
| `periodStartDate` | string | yes | The start of the reporting period in YYYY-MM-DD format. Example: `2026-03-20`. |
| `periodEndDate` | string | no | The end of the reporting period in YYYY-MM-DD format. If omitted, today is used. Example: `2026-03-27`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklists": [
        {}
      ],
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checklists` | array<object> | Checklist analytics rows for the requested period. |
| `tasks` | array<object> | Task analytics rows for the requested period. |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/analytics/all` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics.md) for the provider-specific parameters and requirements.

