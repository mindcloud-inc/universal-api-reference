# SignalWire: List SWML Scripts

Retrieves SWML scripts from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-swml-scripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-swml-scripts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-swml-scripts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `data` | array<object> | An array of objects that contain a list of SWML Script data |
| `links.first` | string | Link to the first page |
| `links.next` | string | Link to the next page |
| `links.prev` | string | Link to the previous page |
| `links.self` | string | Link to the current page |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/swml_scripts` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-swml-scripts.md) for the provider-specific parameters and requirements.

