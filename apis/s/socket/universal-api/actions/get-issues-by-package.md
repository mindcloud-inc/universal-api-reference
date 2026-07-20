# Socket: Get Issues by Package

Retrieves package issue details from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-issues-by-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-issues-by-package?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-issues-by-package?${params}`, {
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
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].type` | string |  |
| `items[].value` | object |  |
| `items[].value.category` | string |  |
| `items[].value.description` | string |  |
| `items[].value.label` | string |  |
| `items[].value.locations` | array<object> |  |
| `items[].value.locations[]` | object |  |
| `items[].value.props` | object |  |
| `items[].value.props.confidence` | number |  |
| `items[].value.props.notes` | string |  |
| `items[].value.props.severity` | number |  |
| `items[].value.severity` | string |  |
| `items[].value.usage` | object |  |
| `items[].value.usage.dependencies` | string |  |
| `items[].value.usage.file` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /npm/:package/:version/issues` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issues-by-package.md) for the provider-specific parameters and requirements.

