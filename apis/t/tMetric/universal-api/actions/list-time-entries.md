# TMetric: List Time Entries



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-time-entries?${params}`, {
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
| `accountId` | number | yes | Workspace identifier. |
| `endDate` | date | no | Filter time entries through this date. |
| `startDate` | date | no | Filter time entries from this date. |
| `userId` | number | no | Optional user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endTime": "string",
      "id": 1,
      "isBillable": true,
      "isInvoiced": true,
      "note": "string",
      "startTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endTime` | string |  |
| `id` | number |  |
| `isBillable` | boolean |  |
| `isInvoiced` | boolean |  |
| `note` | string |  |
| `startTime` | date |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/timeentries` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

