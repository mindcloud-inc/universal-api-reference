# Bookvault: List Bindings

Retrieves available bindings from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-bindings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-bindings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-bindings?${params}`, {
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
      "BindID": 1,
      "Binding": "string",
      "International": {},
      "MaxSpineWidth": 1,
      "Messages": [
        "string"
      ],
      "MinHeight": 1,
      "MinWidth": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BindID` | number |  |
| `Binding` | string |  |
| `International` | object |  |
| `MaxSpineWidth` | number |  |
| `Messages` | array<string> |  |
| `MinHeight` | number |  |
| `MinWidth` | number |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Bindings` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bindings.md) for the provider-specific parameters and requirements.

