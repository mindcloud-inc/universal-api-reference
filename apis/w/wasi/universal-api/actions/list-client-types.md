# Wasi: List Client Types

Retrieves client types from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-client-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-client-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-client-types?${params}`, {
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
      "id_client_type": 1,
      "name": "Ava Chen",
      "nombre": "string",
      "public": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_client_type` | number | Wasi client type identifier. |
| `name` | string | Client type name. |
| `nombre` | string | Localized client type label from Wasi. |
| `public` | boolean | Whether the client type is public in Wasi. |

## Native endpoint

Through the native Wasi API, this operation is `GET /client-type/all` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-types.md) for the provider-specific parameters and requirements.

