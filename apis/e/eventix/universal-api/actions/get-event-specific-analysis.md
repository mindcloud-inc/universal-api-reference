# Eventix: Get analysis of an Event

Retrieves analysis for an Eventix event.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-analysis?connectionId=$CONNECTION_ID&guid=event-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "event-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-analysis?${params}`, {
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
| `guid` | string | yes | The guid of the Event. Example: `event-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generated": "string",
      "locations": [
        {}
      ],
      "metadata": [
        {}
      ],
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generated` | string |  |
| `locations` | array<object> |  |
| `metadata` | array<object> |  |
| `values` | object |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/event/:guid/analysis` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-specific-analysis.md) for the provider-specific parameters and requirements.

