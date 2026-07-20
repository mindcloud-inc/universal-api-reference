# Linkbreakers: List Event Traces

Retrieves a list of event traces from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-event-traces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-event-traces?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-event-traces?${params}`, {
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
| `eventId` | string | yes | The ID of the event to list traces for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "traces": [
        {
          "completedAt": "string",
          "createdAt": "string",
          "eventId": "string",
          "id": "string",
          "linkId": "https://example.com",
          "stepAction": "string",
          "stepData": {},
          "stepKind": "string",
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `traces` | array<object> | Workflow traces for the requested event. |
| `traces[].completedAt` | string |  |
| `traces[].createdAt` | string |  |
| `traces[].eventId` | string |  |
| `traces[].id` | string |  |
| `traces[].linkId` | string |  |
| `traces[].stepAction` | string |  |
| `traces[].stepData` | object |  |
| `traces[].stepKind` | string |  |
| `traces[].updatedAt` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/events/:eventId/traces` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-traces.md) for the provider-specific parameters and requirements.

