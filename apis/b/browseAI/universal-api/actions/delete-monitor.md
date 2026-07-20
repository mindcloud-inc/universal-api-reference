# Browse AI: Delete Monitor

Deletes a monitor from Browse AI.

```
DELETE https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/delete-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/delete-monitor?connectionId=$CONNECTION_ID&robotId=c3689adb-50aa-44af-b265-a7e0d4e5846e&monitorId=e524ab69-4269-4d9d-b3d8-678112a10d29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "monitorId": "e524ab69-4269-4d9d-b3d8-678112a10d29"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/delete-monitor?${params}`, {
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
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |
| `monitorId` | string | yes | Unique monitor ID You can find a monitor's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `e524ab69-4269-4d9d-b3d8-678112a10d29`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageCode": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageCode` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Browse AI API, this operation is `DELETE /robots/:robotId/monitors/:monitorId` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-monitor.md) for the provider-specific parameters and requirements.

