# Quantcast: List Key Events

Retrieves key events from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-key-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-key-events?connectionId=$CONNECTION_ID&accountId=9974296" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "9974296"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-key-events?${params}`, {
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
| `accountId` | number | yes | Quantcast account identifier used to scope key events. Default: `9974296`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keyEvents": {
        "edges": {
          "field": "string",
          "id": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keyEvents` | object | Key events connection returned by Quantcast. |
| `keyEvents.edges` | array<object> | Key event nodes in the result set. |
| `keyEvents.edges.field` | string | Field changed by the key event. |
| `keyEvents.edges.id` | number | Key event identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-key-events.md) for the provider-specific parameters and requirements.

