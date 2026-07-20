# Vincario: List Transmission Types



```
GET https://connect.mindcloud.co/v1/universal/vincario/latest/actions/list-transmission-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vincario `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vincario/latest/actions/list-transmission-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vincario/latest/actions/list-transmission-types?${params}`, {
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
      "id": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Vincario API, this operation is `GET /:apiKey/:controlSum/decode/value-list/enum/enum_transmission.:format` (base URL `https://api.vincario.com/3.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transmission-types.md) for the provider-specific parameters and requirements.

