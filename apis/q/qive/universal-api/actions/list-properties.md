# Qive: List Properties



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-properties?${params}`, {
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
      "key": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `key` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v1/property` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

