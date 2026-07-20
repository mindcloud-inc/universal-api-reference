# AddEvent: List event templates



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/list-event-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/list-event-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/list-event-templates?${params}`, {
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
| `type` | string | no | Template type to return. Default: `event-landing`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AddEvent API returns.

## Native endpoint

Through the native AddEvent API, this operation is `GET /events/templates` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-templates.md) for the provider-specific parameters and requirements.

