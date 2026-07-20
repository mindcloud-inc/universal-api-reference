# pixx.io: Get File State

Retrieves a file state from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-file-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-file-state?connectionId=$CONNECTION_ID&fileStateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileStateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-file-state?${params}`, {
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
| `fileStateId` | number | yes | The pixx.io file state ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileState": {
        "id": 1,
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileState` | object |  |
| `fileState.id` | number |  |
| `fileState.name` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /fileStates/:file_state_id` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-state.md) for the provider-specific parameters and requirements.

