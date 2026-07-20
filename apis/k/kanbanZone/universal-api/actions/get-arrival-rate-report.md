# Kanban Zone: Get Arrival Rate Report

Retrieves an arrival rate report from Kanban Zone.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-arrival-rate-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-arrival-rate-report?connectionId=$CONNECTION_ID&board=string&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-arrival-rate-report?${params}`, {
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
| `board` | string | yes | The board public ID. |
| `start` | date | yes | Start of the time window in ISO 8601 format. |
| `end` | date | yes | End of the time window in ISO 8601 format. |
| `includeCards` | boolean | no | Include card ID arrays in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": [
        "string"
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | array<string> |  |
| `total` | number |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `GET /board/:board/reports/arrival-rate` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-arrival-rate-report.md) for the provider-specific parameters and requirements.

