# CallTrackingMetrics: List Call Setting Number Assignments

Retrieves call setting number assignments from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-call-setting-number-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-call-setting-number-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0&callSettingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "callSettingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-call-setting-number-assignments?${params}`, {
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
| `callSettingId` | string | yes | The call setting ID used to filter assigned numbers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": 1,
      "numbers": [
        [
          "string"
        ]
      ],
      "page": 1,
      "perPage": 1,
      "previousPage": 1,
      "totalEntries": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | number |  |
| `numbers[]` | array |  |
| `page` | number |  |
| `perPage` | number |  |
| `previousPage` | number |  |
| `totalEntries` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/numbers.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-call-setting-number-assignments.md) for the provider-specific parameters and requirements.

