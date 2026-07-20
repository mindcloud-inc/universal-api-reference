# Cryptolens: Get Events

Retrieves analytics events from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-events?${params}`, {
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
| `limit` | number | no | Maximum number of events to return. |
| `startingAfter` | number | no | Cursor for events after the given id. |
| `endingBefore` | number | no | Cursor for events before the given id. |
| `time` | string | no | Unix timestamp or JSON interval filter. |
| `productId` | number | no | Product ID to filter on. |
| `key` | string | no | License key string to filter on. |
| `metadata` | string | no | Metadata string to filter on. |
| `v` | string | no | Method version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "message": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> | List of event objects returned by Get Events. |
| `message` | string | Message returned by Get Events. |
| `result` | number | Result code returned by Get Events. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/ai/GetEvents` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events.md) for the provider-specific parameters and requirements.

