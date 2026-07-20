# GoodDay.work: List Project History

Finds history entries for a GoodDay.work project.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-project-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-project-history?connectionId=$CONNECTION_ID&projectId=4uTCIw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "4uTCIw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-project-history?${params}`, {
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
| `projectId` | string | yes | GoodDay project ID. Default: `4uTCIw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventType": "string",
      "id": "string",
      "momentCreated": "string",
      "params": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventType` | string | History event type. |
| `id` | string | History event ID. |
| `momentCreated` | string | History event timestamp. |
| `params` | object | Event-specific payload. |
| `userId` | string | User associated with the history event. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /project/:projectId/history` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-history.md) for the provider-specific parameters and requirements.

