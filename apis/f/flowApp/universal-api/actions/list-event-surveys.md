# Flow App: List Event Surveys



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-event-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-event-surveys?connectionId=$CONNECTION_ID&sessionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-event-surveys?${params}`, {
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
| `sessionToken` | string | yes | The event session token whose surveys you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymous": true,
      "id": 1,
      "name": "Ava Chen",
      "resultDisplayOption": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonymous` | boolean | Whether survey answers are collected anonymously. |
| `id` | number | Survey ID used to fetch survey response reports for the session. |
| `name` | string | Survey name configured for the event session. |
| `resultDisplayOption` | number | Flow survey result display mode for the session. |
| `text` | string | Optional survey intro text returned by Flow. |

## Native endpoint

Through the native Flow App API, this operation is `GET /reports/events/sessions/surveys/:sessionToken` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-surveys.md) for the provider-specific parameters and requirements.

