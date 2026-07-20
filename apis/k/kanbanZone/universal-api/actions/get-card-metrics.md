# Kanban Zone: Get Card Metrics

Retrieves metrics for a Kanban Zone card.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-card-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-card-metrics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-card-metrics?${params}`, {
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
| `id` | string | yes | Card number or ObjectId. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board` | string | no | Board public ID for mirrored cards. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnId": "string",
      "columnState": "string",
      "columnTitle": "string",
      "endAt": "2026-05-07T12:00:00.000Z",
      "startAt": "2026-05-07T12:00:00.000Z",
      "totalTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnId` | string |  |
| `columnState` | string |  |
| `columnTitle` | string |  |
| `endAt` | date |  |
| `startAt` | date |  |
| `totalTime` | number |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `GET /cards/:id/metrics` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-metrics.md) for the provider-specific parameters and requirements.

