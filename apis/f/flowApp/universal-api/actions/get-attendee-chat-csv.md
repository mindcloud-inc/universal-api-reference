# Flow App: Get Attendee Chat CSV



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-attendee-chat-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-attendee-chat-csv?connectionId=$CONNECTION_ID&sessionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-attendee-chat-csv?${params}`, {
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
| `sessionToken` | string | yes | The event session token for the attendee chat CSV report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | CSV report content returned by Flow. |

## Native endpoint

Through the native Flow App API, this operation is `GET /reports/events/sessions/csv/attendeeChat/:sessionToken` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attendee-chat-csv.md) for the provider-specific parameters and requirements.

