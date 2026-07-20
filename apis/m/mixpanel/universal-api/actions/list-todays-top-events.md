# Mixpanel: List Today's Top Events

Retrieves today's top events from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-todays-top-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-todays-top-events?connectionId=$CONNECTION_ID&type=general" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "general"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-todays-top-events?${params}`, {
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
| `type` | string | yes | Analysis type: general, unique, or average. Example: `general`. |
| `limit` | number | no | Maximum number of events to return. Example: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "amount": 1,
          "event": "string",
          "percentChange": 1
        }
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[].amount` | number | Event count for the current day. |
| `events[].event` | string | Event name. |
| `events[].percentChange` | number | Normalized percent change from yesterday. |
| `type` | string | Analysis type used for the query. |

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/events/top` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-todays-top-events.md) for the provider-specific parameters and requirements.

