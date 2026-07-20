# NileDesk: Get Process Timeline

Retrieves a process or board item timeline in NileDesk.

```
GET https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/get-process-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/get-process-timeline?connectionId=$CONNECTION_ID&process_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "process_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/get-process-timeline?${params}`, {
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
| `process_id` | string | yes | The NileDesk process or board item whose timeline should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /GetProcessTimeline` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process-timeline.md) for the provider-specific parameters and requirements.

