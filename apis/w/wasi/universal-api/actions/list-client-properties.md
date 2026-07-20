# Wasi: List Client Properties

Retrieves properties linked to a client in Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-client-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-client-properties?connectionId=$CONNECTION_ID&client_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "client_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-client-properties?${params}`, {
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
| `client_id` | number | yes | Wasi client ID whose related properties should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_type_label": "string",
      "id_client_type": 1,
      "id_property": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_type_label` | string | Relationship client type label. |
| `id_client_type` | number | Relationship client type identifier. |
| `id_property` | number | Related Wasi property identifier. |
| `title` | string | Related property title. |

## Native endpoint

Through the native Wasi API, this operation is `GET /client/properties/:id_client` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-properties.md) for the provider-specific parameters and requirements.

