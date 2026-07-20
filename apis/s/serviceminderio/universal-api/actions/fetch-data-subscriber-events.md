# serviceminder.io: Fetch Data Subscriber Events

Retrieves data subscriber events from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/fetch-data-subscriber-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/fetch-data-subscriber-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/fetch-data-subscriber-events?${params}`, {
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
| `eventCount` | number | no | Maximum number of data subscriber events to fetch. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clearThroughId` | number | no | Clear events through this identifier after fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clearThroughId": 1,
      "eventCount": 1,
      "events": [
        {}
      ],
      "message": "string",
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clearThroughId` | number |  |
| `eventCount` | number |  |
| `events` | array<object> |  |
| `message` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /datasubscriber/fetch` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-data-subscriber-events.md) for the provider-specific parameters and requirements.

