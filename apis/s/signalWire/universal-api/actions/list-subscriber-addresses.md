# SignalWire: List Subscriber Addresses

Retrieves subscriber addresses from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-subscriber-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-subscriber-addresses?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-subscriber-addresses?${params}`, {
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
| `id` | string | yes | Unique ID of a Subscriber Address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {
        "first": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com",
        "self": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | An array of objects that contain a list of Subscriber addresses |
| `links.first` | string | Link to the first page |
| `links.next` | string | Link to the next page |
| `links.prev` | string | Link of the previous page |
| `links.self` | string | Link of the current page |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/subscribers/{id}/addresses` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-addresses.md) for the provider-specific parameters and requirements.

