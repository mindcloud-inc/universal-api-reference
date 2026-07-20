# Kanban Tool: Delete Time Tracker



```
DELETE https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-time-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-time-tracker?connectionId=$CONNECTION_ID&timeTrackerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeTrackerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/delete-time-tracker?${params}`, {
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
| `timeTrackerId` | number | yes | Kanban Tool time tracker ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "time_tracker": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `time_tracker` | object |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `DELETE /time_trackers/:time_tracker_id.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-tracker.md) for the provider-specific parameters and requirements.

