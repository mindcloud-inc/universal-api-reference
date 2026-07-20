# HoneyHive: Get Events

Finds events in HoneyHive by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-events?connectionId=$CONNECTION_ID&project=string&filters%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "filters[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-events?${params}`, {
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
| `project` | string | yes | Project name associated with the event. |
| `filters[]` | array<object> | yes | Event filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "totalEvents": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |
| `totalEvents` | number |  |

## Native endpoint

Through the native HoneyHive API, this operation is `POST /events/export` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events.md) for the provider-specific parameters and requirements.

